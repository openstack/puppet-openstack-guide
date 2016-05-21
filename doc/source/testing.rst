.. _testing_code:

=======
Testing
=======

Testing is required for all new code. If you want to contribute, but are
unfamiliar with the tests we use, take a time and visit `Unit Tests`_
and `Functional Tests`_ sections and the |ci|_ documentation.


Puppet OpenStack CI will verify your changes, but to save time it is
better to run tests locally before submitting the patch.

.. _ci: http://docs.openstack.org/developer/puppet-openstack-guide/ci.html
.. |ci| replace:: Continuous Integration


Unit Tests
==========

Unit tests are written in ruby, so you need to be familiar with Rspec, below
you can find useful commands to test your code.

Running Rspec
-------------

The following command can be invoked in any module directories to run their
rspec tests (|lint|_, |syntax|_, spec, acceptance, etc). It assumes that both
bundler as well as rubygems (and ruby) are already installed on the system.

.. _lint: http://puppet-lint.com/
.. _syntax: https://puppetlabs.com/blog/verifying-puppet-checking-syntax-and-writing-automated-tests
.. |lint| replace:: *lint*
.. |syntax| replace:: *syntax*
.. code-block:: bash

    mkdir vendor
    export GEM_HOME=vendor
    bundle install
    bundle exec rake lint # Run puppet-lint
    bundle exec rake syntax # Syntax check Puppet manifests and templates
    bundle exec rake spec # Run spec tests in a clean fixtures directory
    bundle exec rake acceptance # Run acceptance tests


This relies on the Puppetfile to install all of the external module
required for testing. The url in this file use the git:// protocol, so this
may need to be updated if you are behind a proxy.

.. note::

   Be advised that your local run can be successful and you can get a -1 from
   Jenkins, because you only run the tests for your Operating System Family.

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
       sudo apt-get install -y libxml2-dev libxslt-dev zlib1g-dev git ruby
       ruby-dev build-essential
       OS_TYPE='trusty'
   fi
   echo "" | sudo tee -a /etc/ssh/sshd_config
   echo "Match address 127.0.0.1" | sudo tee -a /etc/ssh/sshd_config
   echo "    PermitRootLogin without-password" | sudo tee -a
   /etc/ssh/sshd_config
   echo "" | sudo tee -a /etc/ssh/sshd_config
   echo "Match address ::1" | sudo tee -a /etc/ssh/sshd_config
   echo "    PermitRootLogin without-password" | sudo tee -a
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
   sudo gem install bundler --no-rdoc --no-ri --verbose
   mkdir .bundled_gems
   export GEM_HOME=`pwd`/.bundled_gems
   bundle install
   export BEAKER_set=nodepool-$OS_TYPE
   export BEAKER_debug=yes
   bundle exec rspec spec/acceptance


|

The last command runs beaker tests by installing & testing the OpenStack
service.
