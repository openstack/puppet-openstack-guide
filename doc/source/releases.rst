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
| 8.z.y                      | Mitaka                       | yes                    |
+----------------------------+------------------------------+------------------------+
| 9.z.y                      | Newton                       | yes                    |
+----------------------------+------------------------------+------------------------+
| 10.z.y                     | Ocata                        | yes                    |
+----------------------------+------------------------------+------------------------+
| 11.z.y                     | Pike                         | yes (current master)   |
+----------------------------+------------------------------+------------------------+
| 12.z.y                     | Queens                       | Future                 |
+----------------------------+------------------------------+------------------------+

Most Recent Modules releases
============================

+---------------------------------+----------------------------------------------------------------------------------+
| Module Name                     | Last Release                                                                     |
+---------------------------------+----------------------------------------------------------------------------------+
| puppet-aodh_                    | `10.3.0 <http://docs.openstack.org/releasenotes/puppet-aodh/>`__                 |
+---------------------------------+----------------------------------------------------------------------------------+
| puppet-barbican_                | `10.3.0 <http://docs.openstack.org/releasenotes/puppet-barbican/>`__             |
+---------------------------------+----------------------------------------------------------------------------------+
| puppet-ceilometer_              | `10.3.0 <http://docs.openstack.org/releasenotes/puppet-ceilometer/>`__           |
+---------------------------------+----------------------------------------------------------------------------------+
| puppet-ceph_                    | `2.2.1 <http://docs.openstack.org/releasenotes/puppet-ceph/>`__                  |
+---------------------------------+----------------------------------------------------------------------------------+
| puppet-cinder_                  | `10.3.0 <http://docs.openstack.org/releasenotes/puppet-cinder/>`__               |
+---------------------------------+----------------------------------------------------------------------------------+
| puppet-cloudkitty_              | None                                                                             |
+---------------------------------+----------------------------------------------------------------------------------+
| puppet-congress_                | None                                                                             |
+---------------------------------+----------------------------------------------------------------------------------+
| puppet-designate_               | `10.3.0 <http://docs.openstack.org/releasenotes/puppet-designate/>`__            |
+---------------------------------+----------------------------------------------------------------------------------+
| puppet-ec2api_                  | `10.3.0 <http://docs.openstack.org/releasenotes/puppet-ec2api/>`__               |
+---------------------------------+----------------------------------------------------------------------------------+
| puppet-glance_                  | `10.3.0 <http://docs.openstack.org/releasenotes/puppet-glance/>`__               |
+---------------------------------+----------------------------------------------------------------------------------+
| puppet-glare_                   | None                                                                             |
+---------------------------------+----------------------------------------------------------------------------------+
| puppet-gnocchi_                 | `10.3.0 <http://docs.openstack.org/releasenotes/puppet-gnocchi/>`__              |
+---------------------------------+----------------------------------------------------------------------------------+
| puppet-heat_                    | `10.3.0 <http://docs.openstack.org/releasenotes/puppet-heat/>`__                 |
+---------------------------------+----------------------------------------------------------------------------------+
| puppet-horizon_                 | `10.3.0 <http://docs.openstack.org/releasenotes/puppet-horizon/>`__              |
+---------------------------------+----------------------------------------------------------------------------------+
| puppet-ironic_                  | `10.3.0 <http://docs.openstack.org/releasenotes/puppet-ironic/>`__               |
+---------------------------------+----------------------------------------------------------------------------------+
| puppet-keystone_                | `10.3.0 <http://docs.openstack.org/releasenotes/puppet-keystone/>`__             |
+---------------------------------+----------------------------------------------------------------------------------+
| puppet-magnum_                  | `10.3.0 <http://docs.openstack.org/releasenotes/puppet-magnum/>`__               |
+---------------------------------+----------------------------------------------------------------------------------+
| puppet-manila_                  | `10.3.0 <http://docs.openstack.org/releasenotes/puppet-manila/>`__               |
+---------------------------------+----------------------------------------------------------------------------------+
| puppet-mistral_                 | `10.3.0 <http://docs.openstack.org/releasenotes/puppet-mistral/>`__              |
+---------------------------------+----------------------------------------------------------------------------------+
| puppet-murano_                  | `10.3.0 <http://docs.openstack.org/releasenotes/puppet-murano/>`__               |
+---------------------------------+----------------------------------------------------------------------------------+
| puppet-neutron_                 | `10.3.0 <http://docs.openstack.org/releasenotes/puppet-neutron/>`__              |
+---------------------------------+----------------------------------------------------------------------------------+
| puppet-nova_                    | `10.3.0 <http://docs.openstack.org/releasenotes/puppet-nova/>`__                 |
+---------------------------------+----------------------------------------------------------------------------------+
| puppet-octavia_                 | `10.3.0 <http://docs.openstack.org/releasenotes/puppet-octavia/>`__              |
+---------------------------------+----------------------------------------------------------------------------------+
| puppet-openstack-cookiecutter_  | None                                                                             |
+---------------------------------+----------------------------------------------------------------------------------+
| puppet-openstack-integration_   | None                                                                             |
+---------------------------------+----------------------------------------------------------------------------------+
| puppet-openstack_extras_        | `10.3.0 <http://docs.openstack.org/releasenotes/puppet-openstack_extras/>`__     |
+---------------------------------+----------------------------------------------------------------------------------+
| puppet-openstack_spec_helper_   | `9.0.0 <http://docs.openstack.org/releasenotes/puppet-openstack_spec_helper/>`__ |
+---------------------------------+----------------------------------------------------------------------------------+
| puppet-openstacklib_            | `10.3.0 <http://docs.openstack.org/releasenotes/puppet-openstacklib/>`__         |
+---------------------------------+----------------------------------------------------------------------------------+
| puppet-oslo_                    | `10.3.0 <http://docs.openstack.org/releasenotes/puppet-oslo/>`__                 |
+---------------------------------+----------------------------------------------------------------------------------+
| puppet-ovn_                     | `10.3.0 <http://docs.openstack.org/releasenotes/puppet-ova/>`__                  |
+---------------------------------+----------------------------------------------------------------------------------+
| puppet-pacemaker_               | `0.4.0 <http://docs.openstack.org/releasenotes/puppet-pacemaker/>`__             |
+---------------------------------+----------------------------------------------------------------------------------+
| puppet-panko_                   | `10.3.0 <http://docs.openstack.org/releasenotes/puppet-panko/>`__                |
+---------------------------------+----------------------------------------------------------------------------------+
| puppet-qdr_                     | None                                                                             |
+---------------------------------+----------------------------------------------------------------------------------+
| puppet-rally_                   | None                                                                             |
+---------------------------------+----------------------------------------------------------------------------------+
| puppet-sahara_                  | `10.3.0 <http://docs.openstack.org/releasenotes/puppet-sahara/>`__               |
+---------------------------------+----------------------------------------------------------------------------------+
| puppet-swift_                   | `10.3.0 <http://docs.openstack.org/releasenotes/puppet-swift/>`__                |
+---------------------------------+----------------------------------------------------------------------------------+
| puppet-tacker_                  | `10.3.0 <http://docs.openstack.org/releasenotes/puppet-tacker/>`__               |
+---------------------------------+----------------------------------------------------------------------------------+
| puppet-tempest_                 | `10.3.0 <http://docs.openstack.org/releasenotes/puppet-tempest/>`__              |
+---------------------------------+----------------------------------------------------------------------------------+
| puppet-trove_                   | `10.3.0 <http://docs.openstack.org/releasenotes/puppet-trove/>`__                |
+---------------------------------+----------------------------------------------------------------------------------+
| puppet-vitrage_                 | None                                                                             |
+---------------------------------+----------------------------------------------------------------------------------+
| puppet-vswitch_                 | `6.3.0 <http://docs.openstack.org/releasenotes/puppet-vswitch/>`__               |
+---------------------------------+----------------------------------------------------------------------------------+
| puppet-watcher_                 | `10.3.0 <http://docs.openstack.org/releasnotes/puppet-watcher/>`__               |
+---------------------------------+----------------------------------------------------------------------------------+
| puppet-zaqar_                   | `10.3.0 <http://docs.openstack.org/releasenotes/puppet-zaqar/>`__                |
+---------------------------------+----------------------------------------------------------------------------------+

.. _puppet-aodh: https://git.openstack.org/cgit/openstack/puppet-aodh
.. _puppet-barbican: https://git.openstack.org/cgit/openstack/puppet-barbican
.. _puppet-ceilometer: https://git.openstack.org/cgit/openstack/puppet-ceilometer
.. _puppet-ceph: https://git.openstack.org/cgit/openstack/puppet-ceph
.. _puppet-cinder: https://git.openstack.org/cgit/openstack/puppet-cinder
.. _puppet-cloudkitty: https://git.openstack.org/cgit/openstack/puppet-cloudkitty
.. _puppet-congress: https://git.openstack.org/cgit/openstack/puppet-congress
.. _puppet-designate: https://git.openstack.org/cgit/openstack/puppet-designate
.. _puppet-ec2api: https://git.openstack.org/cgit/openstack/puppet-ec2api
.. _puppet-glance: https://git.openstack.org/cgit/openstack/puppet-glance
.. _puppet-glare: https://git.openstack.org/cgit/openstack/puppet-glare
.. _puppet-gnocchi: https://git.openstack.org/cgit/openstack/puppet-gnocchi
.. _puppet-heat: https://git.openstack.org/cgit/openstack/puppet-heat
.. _puppet-horizon: https://git.openstack.org/cgit/openstack/puppet-horizon
.. _puppet-ironic: https://git.openstack.org/cgit/openstack/puppet-ironic
.. _puppet-keystone: https://git.openstack.org/cgit/openstack/puppet-keystone
.. _puppet-magnum: https://git.openstack.org/cgit/openstack/puppet-magnum
.. _puppet-manila: https://git.openstack.org/cgit/openstack/puppet-manila
.. _puppet-mistral: https://git.openstack.org/cgit/openstack/puppet-mistral
.. _puppet-murano: https://git.openstack.org/cgit/openstack/puppet-murano
.. _puppet-neutron: https://git.openstack.org/cgit/openstack/puppet-neutron
.. _puppet-nova: https://git.openstack.org/cgit/openstack/puppet-nova
.. _puppet-octavia: https://git.openstack.org/cgit/openstack/puppet-octavia
.. _puppet-openstack-cookiecutter: https://git.openstack.org/cgit/openstack/puppet-openstack-cookiecutter
.. _puppet-openstack-integration: https://git.openstack.org/cgit/openstack/puppet-openstack-integration
.. _puppet-openstack_extras: https://git.openstack.org/cgit/openstack/puppet-openstack_extras
.. _puppet-openstack_spec_helper: https://git.openstack.org/cgit/openstack/puppet-openstack_spec_helper
.. _puppet-openstacklib: https://git.openstack.org/cgit/openstack/puppet-openstacklib
.. _puppet-oslo: https://git.openstack.org/cgit/openstack/puppet-oslo
.. _puppet-ovn: https://git.openstack.org/cgit/openstack/puppet-ovn
.. _puppet-pacemaker: https://git.openstack.org/cgit/openstack/puppet-pacemaker
.. _puppet-panko: https://git.openstack.org/cgit/openstack/puppet-panko
.. _puppet-qdr: https://git.openstack.org/cgit/openstack/puppet-qdr
.. _puppet-rally: https://git.openstack.org/cgit/openstack/puppet-rally
.. _puppet-sahara: https://git.openstack.org/cgit/openstack/puppet-sahara
.. _puppet-swift: https://git.openstack.org/cgit/openstack/puppet-swift
.. _puppet-tacker: https://git.openstack.org/cgit/openstack/puppet-tacker
.. _puppet-tempest: https://git.openstack.org/cgit/openstack/puppet-tempest
.. _puppet-trove: https://git.openstack.org/cgit/openstack/puppet-trove
.. _puppet-vitrage: https://git.openstack.org/cgit/openstack/puppet-vitrage
.. _puppet-vswitch: https://git.openstack.org/cgit/openstack/puppet-vswitch
.. _puppet-watcher: https://git.openstack.org/cgit/openstack/puppet-watcher
.. _puppet-zaqar: https://git.openstack.org/cgit/openstack/puppet-zaqar

Puppetlabs releases
===================

-  From Kilo, some modules are released and approved_ on
   https://forge.puppetlabs.com/openstack
-  For Juno and before, some modules were released on
   https://forge.puppetlabs.com/stackforge

.. _approved: https://forge.puppetlabs.com/approved

How to release Puppet modules
=============================

- For all modules that need to be released, update metadata.json and reno configuration.
  Example with https://review.openstack.org/#/c/371645

- Submit a release request in openstack/releases project.
  Example with https://review.openstack.org/#/c/371965
.. note:: puppet-ceph should be done separately because the branches track ceph releases and not openstack releases.

Once the release is done, you can see the tarballs here:
https://tarballs.openstack.org

If a new branch has been created, some tasks need to be done:

- Branch openstack/puppet-openstack-integration http://docs.openstack.org/infra/manual/drivers.html#create-stable-branch

- Branch openstack/puppet-openstack_spec_helper and update CI scripts to checkout stable,
  also rake_tasks.rb and beaker_spec_helper.rb to checkout the new branch, .gitreview file
  and release notes to have a page for the stable release, looking for notes in the stable
  branch. Note: the patch has to be done in stable/newton.
  Example with https://review.openstack.org/#/c/377951/

- For all modules and openstack/puppet-openstack-integration, Puppetfile + Gemfile to use the
  new branch, also update .gitreview. Note: the patch has to be done in stable/newton.
  Example with https://review.openstack.org/#/c/377931/
