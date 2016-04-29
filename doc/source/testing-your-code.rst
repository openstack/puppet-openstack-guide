#################
Testing your code
#################

#. `Unit Tests`_
#. `Functional Tests`_


Unit Tests
==========

Unit tests are written in ruby, so you need to be familiar with Rspec, below
you can find usefull comands to test your code.

Running Rspec
-------------

The following command can be invoked in any module diretories to run their
rspec tests (lint, syntax, spec, acceptance, etc). It assumes that both
bundler as well as rubygems (and ruby) are already installed on the system.


.. code-block:: bash

    mkdir vendor
    export GEM_HOME=vendor
    bundle install
    bundle exec rake lint # Run puppet-lint
    bundle exec rake syntax # Syntax check Puppet manifests and templates
    bundle exec rake spec # Run spec tests in a clean fixtures directory
    bundle exec rake acceptance # Run acceptance tests


This relies on the file fixtures.yaml to install all of the external module
required for testing. The url in this file use the git:// protocol, so this
may need to be updated if you are behind a proxy.

.. note::

   Be advised that your local run can be sucessfull and you can get a -1 from
   Jenkis, because you only run the tests for your Operating System Family.

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
