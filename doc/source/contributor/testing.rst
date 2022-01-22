.. _testing_code:

=======
Testing
=======

Testing is required for all new code. If you want to contribute, but are
unfamiliar with the tests we use, take the time to visit the `Unit Tests`_
and `Functional Tests`_ sections and the |ci|_ documentation.


Puppet OpenStack CI will verify your changes, but to save time it is
better to run tests locally before submitting the patch.

.. _ci: /contributor/ci.html
.. |ci| replace:: Continuous Integration


Unit Tests
==========

Unit tests are written in ruby, so you need to be familiar with RSpec. Below
you can find useful commands to test your code.

Running RSpec
-------------

The following command can be invoked in any module directories to run their
RSpec tests (|lint|_, |syntax|_, spec, acceptance, etc). It assumes that both
bundler as well as rubygems (and ruby) are already installed on the system.

.. _lint: http://puppet-lint.com/
.. _syntax: https://puppetlabs.com/blog/verifying-puppet-checking-syntax-and-writing-automated-tests
.. |lint| replace:: *lint*
.. |syntax| replace:: *syntax*
.. code-block:: bash

    bundle install --path ~/vendor/bundle # install all deps in ~/vendor/bundle
    bundle exec rake lint # Run puppet-lint
    bundle exec rake syntax # Syntax check Puppet manifests and templates
    bundle exec rake spec # Run spec tests in a clean fixtures directory
    bundle exec rake acceptance # Run acceptance tests


This relies on the Puppetfile to install all of the external modules
required for testing. The url in this file uses the git:// protocol, so this
may need to be updated if you are behind a proxy.

Please note you might need to install some system dependencies in order to
allow bundle to install the gems.

.. note::

  The ~/vendor/bundle directory will contain all the dependencies, and can be shared with
  multiple projects. Doing so avoids duplication.

  In case you don't want shared libraries, please do the following::

    mkdir vendor
    export GEM_HOME=vendor
    bundle install


.. note::

   Be advised that your local run can be successful and you can get a -1 from
   Jenkins, because you only run the tests for your Operating System Family.

Tiny trick for RSpec
--------------------

You might find the time really long while running the tests. Part of the time is
due to the collection of the required puppet modules for the tests. The cache
directory is cleaned after each (successful) run, and if you're doing multiple changes
with an RSpec run between each, you'd want to keep that cache. This can be done like
that:

.. code-block:: bash

    bundle exec rake spec_prep # download all the dependencies
    bundle exec rake spec_standalone # actually run the test and keep cached modules


The modules are downloaded and cached in the *spec/fixtures/modules/* directory

The best reference for getting started with rspec-puppet can be found here_.

.. _here: http://rspec-puppet.com/

Functional Tests
================

We use beaker to run functional tests, the best reference for getting started
with beaker can be found `here <https://github.com/puppetlabs/beaker/wiki>`__.

Running beaker
--------------

.. code:: bash

   #!/bin/bash
   if [ -f /usr/bin/yum ]; then
       sudo yum -y install libxml2-devel libxslt-devel ruby-devel
       sudo yum -y groupinstall "Development Tools"
       OS_TYPE='centos7'
   elif [ -f /usr/bin/apt-get ]; then
       sudo apt-get update
       sudo apt-get install -y libxml2-dev libxslt-dev zlib1g-dev git ruby \
       ruby-dev build-essential
       OS_TYPE='trusty'
   fi
   echo "" | sudo tee -a /etc/ssh/sshd_config
   echo "Match address 127.0.0.1" | sudo tee -a /etc/ssh/sshd_config
   echo "    PermitRootLogin without-password" | sudo tee -a \
   /etc/ssh/sshd_config
   echo "" | sudo tee -a /etc/ssh/sshd_config
   echo "Match address ::1" | sudo tee -a /etc/ssh/sshd_config
   echo "    PermitRootLogin without-password" | sudo tee -a \
   /etc/ssh/sshd_config
   mkdir -p .ssh
   ssh-keygen -f ~/.ssh/id_rsa -b 2048 -C "beaker key" -P ""
   sudo mkdir -p /root/.ssh
   sudo rm /root/.ssh/authorized_keys
   cat ~/.ssh/id_rsa.pub | sudo tee -a /root/.ssh/authorized_keys
   if [ -f /usr/bin/yum ]; then
       sudo systemctl restart sshd
   elif [ -f /usr/bin/apt-get ]; then
       sudo service ssh restart
   fi
   sudo gem install bundler --no-document --verbose
   mkdir .bundled_gems
   export GEM_HOME=`pwd`/.bundled_gems
   bundle install
   export BEAKER_set=nodepool-$OS_TYPE
   export BEAKER_debug=yes
   bundle exec rspec spec/acceptance


|

The last command runs beaker tests by installing and testing the OpenStack
service.
