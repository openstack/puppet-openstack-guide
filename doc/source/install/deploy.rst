.. _deploy:

===============================
Deploy Puppet OpenStack modules
===============================

Deploy Puppet OpenStack modules, deploy OpenStack with Puppet and test the
setup with Tempest.

* Software requirements:

  * Ubuntu 16.04 LTS or CentOS7 fresh install
  * 'git' installed

* Hardware requirements:

  * At least 4GB of memory, but 8GB is recommended.
  * At least 10GB of storage.

.. code-block:: bash

   $ git clone git://git.openstack.org/openstack/puppet-openstack-integration
   $ cd puppet-openstack-integration
   $ ./all-in-one.sh


More information you can find here_.

.. _here: https://github.com/openstack/puppet-openstack-integration#all-in-one
