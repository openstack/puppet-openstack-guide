========
Releases
========

- `Releases Summary`_
- `Most Recent Modules releases`_
- `Puppetlabs releases`_
- `How to release Puppet modules`_


Releases Summary
================

+----------------------------+------------------------------+------------------------+
| Module Version             | OpenStack Version Codename   | Community Supported    |
+============================+==============================+========================+
| 2.y.z                      | Grizzly                      | no - EOL (2014-03-29)  |
+----------------------------+------------------------------+------------------------+
| 3.y.z                      | Havana                       | no - EOL (2014-09-30)  |
+----------------------------+------------------------------+------------------------+
| 4.y.z                      | Icehouse                     | no - EOL (2015-07-02)  |
+----------------------------+------------------------------+------------------------+
| 5.z.y                      | Juno                         | no - EOL (2015-12-07)  |
+----------------------------+------------------------------+------------------------+
| 6.z.y                      | Kilo                         | no - EOL (2016-05-02)  |
+----------------------------+------------------------------+------------------------+
| 7.z.y                      | Liberty                      | no - EOL (2016-11-17)  |
+----------------------------+------------------------------+------------------------+
| 8.z.y                      | Mitaka                       | no - EOL (2017-04-10)  |
+----------------------------+------------------------------+------------------------+
| 9.z.y                      | Newton                       | no - EOL (2017-10-11)  |
+----------------------------+------------------------------+------------------------+
| 10.z.y                     | Ocata                        | no - EOL (2017-02-26)  |
+----------------------------+------------------------------+------------------------+
| 11.z.y                     | Pike                         | no - EOL (2017-08-30)  |
+----------------------------+------------------------------+------------------------+
| 12.z.y                     | Queens                       | no - EOL (2018-02-28)  |
+----------------------------+------------------------------+------------------------+
| 13.z.y                     | Rocky                        | no - EOL (2018-08-30)  |
+----------------------------+------------------------------+------------------------+
| 14.z.y                     | Stein                        | no - EOL (2019-04-10)  |
+----------------------------+------------------------------+------------------------+
| 15.z.y                     | Train                        | no - EOL (2023-11-02)  |
+----------------------------+------------------------------+------------------------+
| 16.z.y                     | Ussuri                       | no - EOL (2023-11-02)  |
+----------------------------+------------------------------+------------------------+
| 17.z.y                     | Victoria                     | no - EOL (2023-11-02)  |
+----------------------------+------------------------------+------------------------+
| 18.z.y                     | Wallaby                      | yes                    |
+----------------------------+------------------------------+------------------------+
| 19.z.y                     | Xena                         | yes                    |
+----------------------------+------------------------------+------------------------+
| 20.z.y                     | Yoga                         | yes                    |
+----------------------------+------------------------------+------------------------+
| 21.z.y                     | Zed                          | yes                    |
+----------------------------+------------------------------+------------------------+
| 22.z.y                     | 2023.1                       | yes                    |
+----------------------------+------------------------------+------------------------+
| 23.z.y                     | 2023.2                       | yes                    |
+----------------------------+------------------------------+------------------------+
| 24.z.y                     | 2024.1                       | yes (current master)   |
+----------------------------+------------------------------+------------------------+

Most Recent Modules releases
============================

+---------------------------------+----------------------------------------------------------------------------------+
| Module Name                     | Last Release                                                                     |
+---------------------------------+----------------------------------------------------------------------------------+
| puppet-aodh_                    | `23.0.0 <http://docs.openstack.org/releasenotes/puppet-aodh/>`__                 |
+---------------------------------+----------------------------------------------------------------------------------+
| puppet-barbican_                | `23.0.0 <http://docs.openstack.org/releasenotes/puppet-barbican/>`__             |
+---------------------------------+----------------------------------------------------------------------------------+
| puppet-ceilometer_              | `23.0.0 <http://docs.openstack.org/releasenotes/puppet-ceilometer/>`__           |
+---------------------------------+----------------------------------------------------------------------------------+
| puppet-ceph_                    | `5.0.0 <http://docs.openstack.org/releasenotes/puppet-ceph/>`__                  |
+---------------------------------+----------------------------------------------------------------------------------+
| puppet-cinder_                  | `23.0.0 <http://docs.openstack.org/releasenotes/puppet-cinder/>`__               |
+---------------------------------+----------------------------------------------------------------------------------+
| puppet-cloudkitty_              | `12.0.0 <http://docs.openstack.org/releasenotes/puppet-cloudkitty/>`__           |
+---------------------------------+----------------------------------------------------------------------------------+
| puppet-designate_               | `23.0.0 <http://docs.openstack.org/releasenotes/puppet-designate/>`__            |
+---------------------------------+----------------------------------------------------------------------------------+
| puppet-ec2api_                  | `23.0.0 <http://docs.openstack.org/releasenotes/puppet-ec2api/>`__               |
+---------------------------------+----------------------------------------------------------------------------------+
| puppet-glance_                  | `23.0.0 <http://docs.openstack.org/releasenotes/puppet-glance/>`__               |
+---------------------------------+----------------------------------------------------------------------------------+
| puppet-gnocchi_                 | `23.0.0 <http://docs.openstack.org/releasenotes/puppet-gnocchi/>`__              |
+---------------------------------+----------------------------------------------------------------------------------+
| puppet-heat_                    | `23.0.0 <http://docs.openstack.org/releasenotes/puppet-heat/>`__                 |
+---------------------------------+----------------------------------------------------------------------------------+
| puppet-horizon_                 | `23.0.0 <http://docs.openstack.org/releasenotes/puppet-horizon/>`__              |
+---------------------------------+----------------------------------------------------------------------------------+
| puppet-ironic_                  | `23.0.0 <http://docs.openstack.org/releasenotes/puppet-ironic/>`__               |
+---------------------------------+----------------------------------------------------------------------------------+
| puppet-keystone_                | `23.0.0 <http://docs.openstack.org/releasenotes/puppet-keystone/>`__             |
+---------------------------------+----------------------------------------------------------------------------------+
| puppet-magnum_                  | `23.0.0 <http://docs.openstack.org/releasenotes/puppet-magnum/>`__               |
+---------------------------------+----------------------------------------------------------------------------------+
| puppet-manila_                  | `23.0.0 <http://docs.openstack.org/releasenotes/puppet-manila/>`__               |
+---------------------------------+----------------------------------------------------------------------------------+
| puppet-mistral_                 | `23.0.0 <http://docs.openstack.org/releasenotes/puppet-mistral/>`__              |
+---------------------------------+----------------------------------------------------------------------------------+
| puppet-murano_                  | `23.0.0 <http://docs.openstack.org/releasenotes/puppet-murano/>`__               |
+---------------------------------+----------------------------------------------------------------------------------+
| puppet-neutron_                 | `23.0.0 <http://docs.openstack.org/releasenotes/puppet-neutron/>`__              |
+---------------------------------+----------------------------------------------------------------------------------+
| puppet-nova_                    | `23.0.0 <http://docs.openstack.org/releasenotes/puppet-nova/>`__                 |
+---------------------------------+----------------------------------------------------------------------------------+
| puppet-octavia_                 | `23.0.0 <http://docs.openstack.org/releasenotes/puppet-octavia/>`__              |
+---------------------------------+----------------------------------------------------------------------------------+
| puppet-openstack-cookiecutter_  | None                                                                             |
+---------------------------------+----------------------------------------------------------------------------------+
| puppet-openstack-integration_   | None                                                                             |
+---------------------------------+----------------------------------------------------------------------------------+
| puppet-openstack_extras_        | `23.0.0 <http://docs.openstack.org/releasenotes/puppet-openstack_extras/>`__     |
+---------------------------------+----------------------------------------------------------------------------------+
| puppet-openstack_spec_helper_   | None                                                                             |
+---------------------------------+----------------------------------------------------------------------------------+
| puppet-openstacklib_            | `23.0.0 <http://docs.openstack.org/releasenotes/puppet-openstacklib/>`__         |
+---------------------------------+----------------------------------------------------------------------------------+
| puppet-oslo_                    | `23.0.0 <http://docs.openstack.org/releasenotes/puppet-oslo/>`__                 |
+---------------------------------+----------------------------------------------------------------------------------+
| puppet-ovn_                     | `23.0.0 <http://docs.openstack.org/releasenotes/puppet-ova/>`__                  |
+---------------------------------+----------------------------------------------------------------------------------+
| puppet-placement_               | `10.0.0 <http://docs.openstack.org/releasenotes/puppet-placement/>`__            |
+---------------------------------+----------------------------------------------------------------------------------+
| puppet-qdr_                     | `12.0.0 <http://docs.openstack.org/releasenotes/puppet-qdr/>`__                  |
+---------------------------------+----------------------------------------------------------------------------------+
| puppet-sahara_                  | `23.0.0 <http://docs.openstack.org/releasenotes/puppet-sahara/>`__               |
+---------------------------------+----------------------------------------------------------------------------------+
| puppet-swift_                   | `23.0.0 <http://docs.openstack.org/releasenotes/puppet-swift/>`__                |
+---------------------------------+----------------------------------------------------------------------------------+
| puppet-tempest_                 | `23.0.0 <http://docs.openstack.org/releasenotes/puppet-tempest/>`__              |
+---------------------------------+----------------------------------------------------------------------------------+
| puppet-trove_                   | `23.0.0 <http://docs.openstack.org/releasenotes/puppet-trove/>`__                |
+---------------------------------+----------------------------------------------------------------------------------+
| puppet-vitrage_                 | `13.0.0 <http://docs.openstack.org/releasenotes/puppet-vitrage/>`__              |
+---------------------------------+----------------------------------------------------------------------------------+
| puppet-vswitch_                 | `19.0.0 <http://docs.openstack.org/releasenotes/puppet-vswitch/>`__              |
+---------------------------------+----------------------------------------------------------------------------------+
| puppet-watcher_                 | `23.0.0 <http://docs.openstack.org/releasnotes/puppet-watcher/>`__               |
+---------------------------------+----------------------------------------------------------------------------------+
| puppet-zaqar_                   | `23.0.0 <http://docs.openstack.org/releasenotes/puppet-zaqar/>`__                |
+---------------------------------+----------------------------------------------------------------------------------+

.. _puppet-aodh: https://opendev.org/openstack/puppet-aodh
.. _puppet-barbican: https://opendev.org/openstack/puppet-barbican
.. _puppet-ceilometer: https://opendev.org/openstack/puppet-ceilometer
.. _puppet-ceph: https://opendev.org/openstack/puppet-ceph
.. _puppet-cinder: https://opendev.org/openstack/puppet-cinder
.. _puppet-cloudkitty: https://opendev.org/openstack/puppet-cloudkitty
.. _puppet-designate: https://opendev.org/openstack/puppet-designate
.. _puppet-ec2api: https://opendev.org/openstack/puppet-ec2api
.. _puppet-glance: https://opendev.org/openstack/puppet-glance
.. _puppet-gnocchi: https://opendev.org/openstack/puppet-gnocchi
.. _puppet-heat: https://opendev.org/openstack/puppet-heat
.. _puppet-horizon: https://opendev.org/openstack/puppet-horizon
.. _puppet-ironic: https://opendev.org/openstack/puppet-ironic
.. _puppet-keystone: https://opendev.org/openstack/puppet-keystone
.. _puppet-magnum: https://opendev.org/openstack/puppet-magnum
.. _puppet-manila: https://opendev.org/openstack/puppet-manila
.. _puppet-mistral: https://opendev.org/openstack/puppet-mistral
.. _puppet-murano: https://opendev.org/openstack/puppet-murano
.. _puppet-neutron: https://opendev.org/openstack/puppet-neutron
.. _puppet-nova: https://opendev.org/openstack/puppet-nova
.. _puppet-octavia: https://opendev.org/openstack/puppet-octavia
.. _puppet-openstack-cookiecutter: https://opendev.org/openstack/puppet-openstack-cookiecutter
.. _puppet-openstack-integration: https://opendev.org/openstack/puppet-openstack-integration
.. _puppet-openstack_extras: https://opendev.org/openstack/puppet-openstack_extras
.. _puppet-openstack_spec_helper: https://opendev.org/openstack/puppet-openstack_spec_helper
.. _puppet-openstacklib: https://opendev.org/openstack/puppet-openstacklib
.. _puppet-oslo: https://opendev.org/openstack/puppet-oslo
.. _puppet-ovn: https://opendev.org/openstack/puppet-ovn
.. _puppet-placement: https://opendev.org/openstack/puppet-placement
.. _puppet-qdr: https://opendev.org/openstack/puppet-qdr
.. _puppet-sahara: https://opendev.org/openstack/puppet-sahara
.. _puppet-swift: https://opendev.org/openstack/puppet-swift
.. _puppet-tempest: https://opendev.org/openstack/puppet-tempest
.. _puppet-trove: https://opendev.org/openstack/puppet-trove
.. _puppet-vitrage: https://opendev.org/openstack/puppet-vitrage
.. _puppet-vswitch: https://opendev.org/openstack/puppet-vswitch
.. _puppet-watcher: https://opendev.org/openstack/puppet-watcher
.. _puppet-zaqar: https://opendev.org/openstack/puppet-zaqar

Puppetlabs releases
===================

-  From Stein, all new releases are automatically uploaded on
   https://forge.puppetlabs.com/openstack
-  From Kilo, some modules are released and approved_ on
   https://forge.puppetlabs.com/openstack
-  For Juno and before, some modules were released on
   https://forge.puppetlabs.com/stackforge

.. _approved: https://forge.puppetlabs.com/approved

How to release Puppet modules
=============================

- For all modules that need to be released, update metadata.json.
  Example with https://review.opendev.org/#/c/545917

- Submit a release request in openstack/releases project.
  Example with https://review.opendev.org/#/c/546178/

.. note:: puppet-ceph should be done separately because the branches track ceph
          releases and not openstack releases.

Once the release is done, you can see the tarballs here:
https://tarballs.openstack.org

If a new branch has been created, some tasks need to be done:

- Branch openstack/puppet-openstack-integration and openstack/puppet-openstack_spec_helper
  http://docs.openstack.org/infra/manual/drivers.html#create-stable-branch

- Update openstack/puppet-openstack_spec_helper and update CI scripts to checkout stable,
  also rake_tasks.rb to checkout the new branch, .gitreview file and release notes to
  have a page for the stable release, looking for notes in the stable branch.
  Note: the patch has to be done in stable/pike.
  Example: https://review.opendev.org/#/c/497403/

- Update Puppetfile in openstack/puppet-openstack-integration

- Update this documentation
