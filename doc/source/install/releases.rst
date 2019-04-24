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
| 10.z.y                     | Ocata                        | yes - EOL (2017-02-26) |
+----------------------------+------------------------------+------------------------+
| 11.z.y                     | Pike                         | yes - EOL (2017-08-30) |
+----------------------------+------------------------------+------------------------+
| 12.z.y                     | Queens                       | yes - EOL (2018-02-28) |
+----------------------------+------------------------------+------------------------+
| 13.z.y                     | Rocky                        | yes - EOL (2019-02-23) |
+----------------------------+------------------------------+------------------------+
| 14.z.y                     | Stein                        | yes                    |
+----------------------------+------------------------------+------------------------+
| 15.z.y                     | Train                        | yes (current master)   |
+----------------------------+------------------------------+------------------------+

Most Recent Modules releases
============================

+---------------------------------+----------------------------------------------------------------------------------+
| Module Name                     | Last Release                                                                     |
+---------------------------------+----------------------------------------------------------------------------------+
| puppet-aodh_                    | `14.4.0 <http://docs.openstack.org/releasenotes/puppet-aodh/>`__                 |
+---------------------------------+----------------------------------------------------------------------------------+
| puppet-barbican_                | `14.4.0 <http://docs.openstack.org/releasenotes/puppet-barbican/>`__             |
+---------------------------------+----------------------------------------------------------------------------------+
| puppet-ceilometer_              | `14.4.0 <http://docs.openstack.org/releasenotes/puppet-ceilometer/>`__           |
+---------------------------------+----------------------------------------------------------------------------------+
| puppet-ceph_                    | `2.6.0 <http://docs.openstack.org/releasenotes/puppet-ceph/>`__                  |
+---------------------------------+----------------------------------------------------------------------------------+
| puppet-cinder_                  | `14.4.0 <http://docs.openstack.org/releasenotes/puppet-cinder/>`__               |
+---------------------------------+----------------------------------------------------------------------------------+
| puppet-cloudkitty_              | `3.4.0 <http://docs.openstack.org/releasenotes/puppet-cloudkitty/>`__            |
+---------------------------------+----------------------------------------------------------------------------------+
| puppet-congress_                | `14.4.0 <http://docs.openstack.org/releasenotes/puppet-congress/>`__             |
+---------------------------------+----------------------------------------------------------------------------------+
| puppet-designate_               | `14.4.0 <http://docs.openstack.org/releasenotes/puppet-designate/>`__            |
+---------------------------------+----------------------------------------------------------------------------------+
| puppet-ec2api_                  | `14.4.0 <http://docs.openstack.org/releasenotes/puppet-ec2api/>`__               |
+---------------------------------+----------------------------------------------------------------------------------+
| puppet-freezer_                 | `3.4.0 <http://docs.openstack.org/releasenotes/puppet-freezer/>`__               |
+---------------------------------+----------------------------------------------------------------------------------+
| puppet-glance_                  | `14.4.0 <http://docs.openstack.org/releasenotes/puppet-glance/>`__               |
+---------------------------------+----------------------------------------------------------------------------------+
| puppet-glare_                   | `3.4.0 <http://docs.openstack.org/releasenotes/puppet-glare/>`__                |
+---------------------------------+----------------------------------------------------------------------------------+
| puppet-gnocchi_                 | `14.4.0 <http://docs.openstack.org/releasenotes/puppet-gnocchi/>`__              |
+---------------------------------+----------------------------------------------------------------------------------+
| puppet-heat_                    | `14.4.0 <http://docs.openstack.org/releasenotes/puppet-heat/>`__                 |
+---------------------------------+----------------------------------------------------------------------------------+
| puppet-horizon_                 | `14.4.0 <http://docs.openstack.org/releasenotes/puppet-horizon/>`__              |
+---------------------------------+----------------------------------------------------------------------------------+
| puppet-ironic_                  | `14.4.0 <http://docs.openstack.org/releasenotes/puppet-ironic/>`__               |
+---------------------------------+----------------------------------------------------------------------------------+
| puppet-keystone_                | `14.4.0 <http://docs.openstack.org/releasenotes/puppet-keystone/>`__             |
+---------------------------------+----------------------------------------------------------------------------------+
| puppet-magnum_                  | `14.4.0 <http://docs.openstack.org/releasenotes/puppet-magnum/>`__               |
+---------------------------------+----------------------------------------------------------------------------------+
| puppet-manila_                  | `14.4.0 <http://docs.openstack.org/releasenotes/puppet-manila/>`__               |
+---------------------------------+----------------------------------------------------------------------------------+
| puppet-mistral_                 | `14.4.0 <http://docs.openstack.org/releasenotes/puppet-mistral/>`__              |
+---------------------------------+----------------------------------------------------------------------------------+
| puppet-monasca_                 | `3.4.0 <http://docs.openstack.org/releasenotes/puppet-monasca/>`__               |
+---------------------------------+----------------------------------------------------------------------------------+
| puppet-murano_                  | `14.4.0 <http://docs.openstack.org/releasenotes/puppet-murano/>`__               |
+---------------------------------+----------------------------------------------------------------------------------+
| puppet-neutron_                 | `14.4.0 <http://docs.openstack.org/releasenotes/puppet-neutron/>`__              |
+---------------------------------+----------------------------------------------------------------------------------+
| puppet-nova_                    | `14.4.0 <http://docs.openstack.org/releasenotes/puppet-nova/>`__                 |
+---------------------------------+----------------------------------------------------------------------------------+
| puppet-octavia_                 | `14.4.0 <http://docs.openstack.org/releasenotes/puppet-octavia/>`__              |
+---------------------------------+----------------------------------------------------------------------------------+
| puppet-openstack-cookiecutter_  | None                                                                             |
+---------------------------------+----------------------------------------------------------------------------------+
| puppet-openstack-integration_   | None                                                                             |
+---------------------------------+----------------------------------------------------------------------------------+
| puppet-openstack_extras_        | `14.4.0 <http://docs.openstack.org/releasenotes/puppet-openstack_extras/>`__     |
+---------------------------------+----------------------------------------------------------------------------------+
| puppet-openstack_spec_helper_   | `14.0.0 <http://docs.openstack.org/releasenotes/puppet-openstack_spec_helper/>`__|
+---------------------------------+----------------------------------------------------------------------------------+
| puppet-openstacklib_            | `14.4.0 <http://docs.openstack.org/releasenotes/puppet-openstacklib/>`__         |
+---------------------------------+----------------------------------------------------------------------------------+
| puppet-oslo_                    | `14.4.0 <http://docs.openstack.org/releasenotes/puppet-oslo/>`__                 |
+---------------------------------+----------------------------------------------------------------------------------+
| puppet-ovn_                     | `14.4.0 <http://docs.openstack.org/releasenotes/puppet-ova/>`__                  |
+---------------------------------+----------------------------------------------------------------------------------+
| puppet-panko_                   | `14.4.0 <http://docs.openstack.org/releasenotes/puppet-panko/>`__                |
+---------------------------------+----------------------------------------------------------------------------------+
| puppet-qdr_                     | `3.4.0 <http://docs.openstack.org/releasenotes/puppet-qdr/>`__                   |
+---------------------------------+----------------------------------------------------------------------------------+
| puppet-rally_                   | `2.4.0 <http://docs.openstack.org/releasenotes/puppet-rally/>`__                 |
+---------------------------------+----------------------------------------------------------------------------------+
| puppet-sahara_                  | `14.4.0 <http://docs.openstack.org/releasenotes/puppet-sahara/>`__               |
+---------------------------------+----------------------------------------------------------------------------------+
| puppet-senlin_                  | `1.2.0 <http://docs.openstack.org/releasenotes/puppet-senlin/>`__                |
+---------------------------------+----------------------------------------------------------------------------------+
| puppet-swift_                   | `14.4.0 <http://docs.openstack.org/releasenotes/puppet-swift/>`__                |
+---------------------------------+----------------------------------------------------------------------------------+
| puppet-tacker_                  | `14.4.0 <http://docs.openstack.org/releasenotes/puppet-tacker/>`__               |
+---------------------------------+----------------------------------------------------------------------------------+
| puppet-tempest_                 | `14.4.0 <http://docs.openstack.org/releasenotes/puppet-tempest/>`__              |
+---------------------------------+----------------------------------------------------------------------------------+
| puppet-trove_                   | `14.4.0 <http://docs.openstack.org/releasenotes/puppet-trove/>`__                |
+---------------------------------+----------------------------------------------------------------------------------+
| puppet-vitrage_                 | `4.4.0 <http://docs.openstack.org/releasenotes/puppet-vitrage/>`__               |
+---------------------------------+----------------------------------------------------------------------------------+
| puppet-vswitch_                 | `10.4.0 <http://docs.openstack.org/releasenotes/puppet-vswitch/>`__               |
+---------------------------------+----------------------------------------------------------------------------------+
| puppet-watcher_                 | `14.4.0 <http://docs.openstack.org/releasnotes/puppet-watcher/>`__               |
+---------------------------------+----------------------------------------------------------------------------------+
| puppet-zaqar_                   | `14.4.0 <http://docs.openstack.org/releasenotes/puppet-zaqar/>`__                |
+---------------------------------+----------------------------------------------------------------------------------+

.. _puppet-aodh: https://opendev.org/openstack/puppet-aodh
.. _puppet-barbican: https://opendev.org/openstack/puppet-barbican
.. _puppet-ceilometer: https://opendev.org/openstack/puppet-ceilometer
.. _puppet-ceph: https://opendev.org/openstack/puppet-ceph
.. _puppet-cinder: https://opendev.org/openstack/puppet-cinder
.. _puppet-cloudkitty: https://opendev.org/openstack/puppet-cloudkitty
.. _puppet-congress: https://opendev.org/openstack/puppet-congress
.. _puppet-designate: https://opendev.org/openstack/puppet-designate
.. _puppet-ec2api: https://opendev.org/openstack/puppet-ec2api
.. _puppet-freezer: https://opendev.org/openstack/puppet-freezer
.. _puppet-glance: https://opendev.org/openstack/puppet-glance
.. _puppet-glare: https://opendev.org/openstack/puppet-glare
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
.. _puppet-panko: https://opendev.org/openstack/puppet-panko
.. _puppet-qdr: https://opendev.org/openstack/puppet-qdr
.. _puppet-rally: https://opendev.org/openstack/puppet-rally
.. _puppet-sahara: https://opendev.org/openstack/puppet-sahara
.. _puppet-senlin: https://opendev.org/openstack/puppet-senlin
.. _puppet-swift: https://opendev.org/openstack/puppet-swift
.. _puppet-tacker: https://opendev.org/openstack/puppet-tacker
.. _puppet-tempest: https://opendev.org/openstack/puppet-tempest
.. _puppet-trove: https://opendev.org/openstack/puppet-trove
.. _puppet-vitrage: https://opendev.org/openstack/puppet-vitrage
.. _puppet-vswitch: https://opendev.org/openstack/puppet-vswitch
.. _puppet-watcher: https://opendev.org/openstack/puppet-watcher
.. _puppet-zaqar: https://opendev.org/openstack/puppet-zaqar

Puppetlabs releases
===================

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
.. note:: puppet-pacemaker should also be done seperately because it is an
          independent release

Once the release is done, you can see the tarballs here:
https://tarballs.openstack.org

If a new branch has been created, some tasks need to be done:

- Update the gerrit bot to pick up changes for the new stable branch.
  Example: https://review.opendev.org/#/c/497411/

- Branch openstack/puppet-openstack-integration and openstack/puppet-openstack_spec_helper
  http://docs.openstack.org/infra/manual/drivers.html#create-stable-branch

- Update openstack/puppet-openstack_spec_helper and update CI scripts to checkout stable,
  also rake_tasks.rb and beaker_spec_helper.rb to checkout the new branch, .gitreview file
  and release notes to have a page for the stable release, looking for notes in the stable
  branch. Note: the patch has to be done in stable/pike.
  Example: https://review.opendev.org/#/c/497403/

- For all modules and openstack/puppet-openstack-integration, Puppetfile + Gemfile to use the
  new branch, also update .gitreview. Note: example patches patch has to be done in stable/pike.
  Example: https://review.opendev.org/#/q/topic:switch-to-pike

- Update this documentation
