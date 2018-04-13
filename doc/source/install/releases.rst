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
| 9.z.y                      | Newton                       | yes - EOL (2017-10-11) |
+----------------------------+------------------------------+------------------------+
| 10.z.y                     | Ocata                        | yes - EOL (2017-02-26) |
+----------------------------+------------------------------+------------------------+
| 11.z.y                     | Pike                         | yes - EOL (2017-08-30) |
+----------------------------+------------------------------+------------------------+
| 12.z.y                     | Queens                       | yes - EOL (2018-02-28) |
+----------------------------+------------------------------+------------------------+
| 13.z.y                     | Rocky                        | yes (current master)   |
+----------------------------+------------------------------+------------------------+
| 14.z.y                     | Solar                        | Future                 |
+----------------------------+------------------------------+------------------------+

Most Recent Modules releases
============================

+---------------------------------+----------------------------------------------------------------------------------+
| Module Name                     | Last Release                                                                     |
+---------------------------------+----------------------------------------------------------------------------------+
| puppet-aodh_                    | `12.4.0 <http://docs.openstack.org/releasenotes/puppet-aodh/>`__                 |
+---------------------------------+----------------------------------------------------------------------------------+
| puppet-barbican_                | `12.4.0 <http://docs.openstack.org/releasenotes/puppet-barbican/>`__             |
+---------------------------------+----------------------------------------------------------------------------------+
| puppet-ceilometer_              | `12.5.0 <http://docs.openstack.org/releasenotes/puppet-ceilometer/>`__           |
+---------------------------------+----------------------------------------------------------------------------------+
| puppet-ceph_                    | `2.5.0 <http://docs.openstack.org/releasenotes/puppet-ceph/>`__                  |
+---------------------------------+----------------------------------------------------------------------------------+
| puppet-cinder_                  | `12.4.0 <http://docs.openstack.org/releasenotes/puppet-cinder/>`__               |
+---------------------------------+----------------------------------------------------------------------------------+
| puppet-cloudkitty_              | `1.0.0 <http://docs.openstack.org/releasenotes/puppet-cloudkitty/>`__            |
+---------------------------------+----------------------------------------------------------------------------------+
| puppet-congress_                | `12.4.0 <http://docs.openstack.org/releasenotes/puppet-congress/>`__             |
+---------------------------------+----------------------------------------------------------------------------------+
| puppet-designate_               | `12.4.0 <http://docs.openstack.org/releasenotes/puppet-designate/>`__            |
+---------------------------------+----------------------------------------------------------------------------------+
| puppet-ec2api_                  | `12.4.0 <http://docs.openstack.org/releasenotes/puppet-ec2api/>`__               |
+---------------------------------+----------------------------------------------------------------------------------+
| puppet-freezer_                 | `1.0.0 <http://docs.openstack.org/releasenotes/puppet-freezer/>`__               |
+---------------------------------+----------------------------------------------------------------------------------+
| puppet-glance_                  | `12.5.0 <http://docs.openstack.org/releasenotes/puppet-glance/>`__               |
+---------------------------------+----------------------------------------------------------------------------------+
| puppet-glare_                   | `1.0.0 <http://docs.openstack.org/releasenotes/puppet-glare/>`__                 |
+---------------------------------+----------------------------------------------------------------------------------+
| puppet-gnocchi_                 | `12.4.0 <http://docs.openstack.org/releasenotes/puppet-gnocchi/>`__              |
+---------------------------------+----------------------------------------------------------------------------------+
| puppet-heat_                    | `12.4.0 <http://docs.openstack.org/releasenotes/puppet-heat/>`__                 |
+---------------------------------+----------------------------------------------------------------------------------+
| puppet-horizon_                 | `12.4.0 <http://docs.openstack.org/releasenotes/puppet-horizon/>`__              |
+---------------------------------+----------------------------------------------------------------------------------+
| puppet-ironic_                  | `12.4.0 <http://docs.openstack.org/releasenotes/puppet-ironic/>`__               |
+---------------------------------+----------------------------------------------------------------------------------+
| puppet-keystone_                | `12.4.0 <http://docs.openstack.org/releasenotes/puppet-keystone/>`__             |
+---------------------------------+----------------------------------------------------------------------------------+
| puppet-magnum_                  | `12.2.0 <http://docs.openstack.org/releasenotes/puppet-magnum/>`__               |
+---------------------------------+----------------------------------------------------------------------------------+
| puppet-manila_                  | `12.4.0 <http://docs.openstack.org/releasenotes/puppet-manila/>`__               |
+---------------------------------+----------------------------------------------------------------------------------+
| puppet-mistral_                 | `12.4.0 <http://docs.openstack.org/releasenotes/puppet-mistral/>`__              |
+---------------------------------+----------------------------------------------------------------------------------+
| puppet-monasca_                 | `1.1.0 <http://docs.openstack.org/releasenotes/puppet-monasca/>`__               |
+---------------------------------+----------------------------------------------------------------------------------+
| puppet-murano_                  | `12.4.0 <http://docs.openstack.org/releasenotes/puppet-murano/>`__               |
+---------------------------------+----------------------------------------------------------------------------------+
| puppet-neutron_                 | `12.4.0 <http://docs.openstack.org/releasenotes/puppet-neutron/>`__              |
+---------------------------------+----------------------------------------------------------------------------------+
| puppet-nova_                    | `12.4.0 <http://docs.openstack.org/releasenotes/puppet-nova/>`__                 |
+---------------------------------+----------------------------------------------------------------------------------+
| puppet-octavia_                 | `12.4.0 <http://docs.openstack.org/releasenotes/puppet-octavia/>`__              |
+---------------------------------+----------------------------------------------------------------------------------+
| puppet-openstack-cookiecutter_  | None                                                                             |
+---------------------------------+----------------------------------------------------------------------------------+
| puppet-openstack-integration_   | None                                                                             |
+---------------------------------+----------------------------------------------------------------------------------+
| puppet-openstack_extras_        | `12.4.0 <http://docs.openstack.org/releasenotes/puppet-openstack_extras/>`__     |
+---------------------------------+----------------------------------------------------------------------------------+
| puppet-openstack_spec_helper_   | `12.0.0 <http://docs.openstack.org/releasenotes/puppet-openstack_spec_helper/>`__|
+---------------------------------+----------------------------------------------------------------------------------+
| puppet-openstacklib_            | `12.4.0 <http://docs.openstack.org/releasenotes/puppet-openstacklib/>`__         |
+---------------------------------+----------------------------------------------------------------------------------+
| puppet-oslo_                    | `12.4.0 <http://docs.openstack.org/releasenotes/puppet-oslo/>`__                 |
+---------------------------------+----------------------------------------------------------------------------------+
| puppet-ovn_                     | `12.4.0 <http://docs.openstack.org/releasenotes/puppet-ova/>`__                  |
+---------------------------------+----------------------------------------------------------------------------------+
| puppet-panko_                   | `12.4.0 <http://docs.openstack.org/releasenotes/puppet-panko/>`__                |
+---------------------------------+----------------------------------------------------------------------------------+
| puppet-qdr_                     | `1.0.0 <http://docs.openstack.org/releasenotes/puppet-qdr/>`__                   |
+---------------------------------+----------------------------------------------------------------------------------+
| puppet-rally_                   | `0.1.0 <http://docs.openstack.org/releasenotes/puppet-rally/>`__                 |
+---------------------------------+----------------------------------------------------------------------------------+
| puppet-sahara_                  | `12.4.0 <http://docs.openstack.org/releasenotes/puppet-sahara/>`__               |
+---------------------------------+----------------------------------------------------------------------------------+
| puppet-swift_                   | `12.4.0 <http://docs.openstack.org/releasenotes/puppet-swift/>`__                |
+---------------------------------+----------------------------------------------------------------------------------+
| puppet-tacker_                  | `12.4.0 <http://docs.openstack.org/releasenotes/puppet-tacker/>`__               |
+---------------------------------+----------------------------------------------------------------------------------+
| puppet-tempest_                 | `12.5.0 <http://docs.openstack.org/releasenotes/puppet-tempest/>`__              |
+---------------------------------+----------------------------------------------------------------------------------+
| puppet-trove_                   | `12.4.0 <http://docs.openstack.org/releasenotes/puppet-trove/>`__                |
+---------------------------------+----------------------------------------------------------------------------------+
| puppet-vitrage_                 | `2.4.0 <http://docs.openstack.org/releasenotes/puppet-vitrage/>`__               |
+---------------------------------+----------------------------------------------------------------------------------+
| puppet-vswitch_                 | `8.4.0 <http://docs.openstack.org/releasenotes/puppet-vswitch/>`__               |
+---------------------------------+----------------------------------------------------------------------------------+
| puppet-watcher_                 | `12.4.0 <http://docs.openstack.org/releasnotes/puppet-watcher/>`__               |
+---------------------------------+----------------------------------------------------------------------------------+
| puppet-zaqar_                   | `12.4.0 <http://docs.openstack.org/releasenotes/puppet-zaqar/>`__                |
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
.. _puppet-freezer: https://git.openstack.org/cgit/openstack/puppet-freezer
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

- For all modules that need to be released, update metadata.json.
  Example with https://review.openstack.org/#/c/545917

- Submit a release request in openstack/releases project.
  Example with https://review.openstack.org/#/c/546178/

.. note:: puppet-ceph should be done separately because the branches track ceph
          releases and not openstack releases.
.. note:: puppet-pacemaker should also be done seperately because it is an
          independent release

Once the release is done, you can see the tarballs here:
https://tarballs.openstack.org

If a new branch has been created, some tasks need to be done:

- Update the gerrit bot to pick up changes for the new stable branch.
  Example: https://review.openstack.org/#/c/497411/

- Branch openstack/puppet-openstack-integration and openstack/puppet-openstack_spec_helper
  http://docs.openstack.org/infra/manual/drivers.html#create-stable-branch

- Update openstack/puppet-openstack_spec_helper and update CI scripts to checkout stable,
  also rake_tasks.rb and beaker_spec_helper.rb to checkout the new branch, .gitreview file
  and release notes to have a page for the stable release, looking for notes in the stable
  branch. Note: the patch has to be done in stable/pike.
  Example: https://review.openstack.org/#/c/497403/

- For all modules and openstack/puppet-openstack-integration, Puppetfile + Gemfile to use the
  new branch, also update .gitreview. Note: example patches patch has to be done in stable/pike.
  Example: https://review.openstack.org/#/q/topic:switch-to-pike

- Update this documentation
