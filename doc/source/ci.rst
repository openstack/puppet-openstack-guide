.. _ci:

######################
Continuous Integration
######################


This is a list of the CI jobs that are running against most of the Puppet
OpenStack modules: The code that configures Jenkins jobs is hosted by
`project-config
<http://git.openstack.org/cgit/openstack-infra/project-config/tree/jenkins
/jobs/puppet-module-jobs.yaml>`__.

.. list-table:: **CI Jobs in puppet-openstack**
   :widths: 12 25 8 55
   :header-rows: 1

   * - Job name
     - Description
     - Voting
     - What to do in case of failure
   * - gate-puppet-puppet-lint
     - It makes sure the code follows recommended `Puppet style guidelines
       <http://docs.puppetlabs.com/guides/style_guide.html>`__
     - Yes
     - Read the job logs to see where the code does not follow the Puppet lint
       style.
   * - gate-puppet-puppet-syntax-{3,4}
     - Syntax checks for Puppet manifests, templates, and Hiera YAML. The jobs
       run on the latest Puppet 3.x and 4.x releases.
     - Yes
     - Read the job logs to see where the code does not follow the Puppet
       syntax style.
   * - gate-puppet-puppet-unit-{3.6,3.8,4.5}
     - RSpec tests for Puppet manifests.
     - Yes
     - Read the job logs to see where the tests are failing. `More
       documentation about RSpec <http://rspec-puppet.com/tutorial/>`__
   * - gate-puppet-puppet-unit-latest
     - RSpec tests for Puppet manifests. The jobs run on the latest version
       of Puppet. It aims to be experimental to track any work to do in the
       module to be compatible with the latest release of Puppet.
     - No
     - Read the job logs to see where the tests are failing. Even though the
       job is non-voting, please raise a bug in Launchpad to make sure someone
       has a look and maybe update the module to work with latest version of
       Puppet.
   * - gate-puppet-puppet-beaker-rspec-dsvm-{centos7,trusty,xenial}
     - Beaker jobs to do functional testing. It will prepare the Puppet
       environment on 2 different systems (CentOS 7 and Ubuntu Trusty), run
       Puppet to configure the module resources and run some tests with
       serverspec.
     - Yes
     - Read the job logs. Sometimes, the job fails because of packaging issues
       or mirrors downtime. Please report a bug for this so we can find
       workarounds. Otherwise, make sure your patch is supposed to work with
       current tests or you'll have to adapt the tests to change the expected
       behavior. `More documentation about Beaker
       <https://github.com/puppetlabs/beaker/wiki>`__
   * - gate-puppet-openstack-integration-{3,4}-scenarioX-tempest-dsvm-{centos7
       ,trusty,xenial}
     - Functional testing jobs that will deploy OpenStack run tempest smoke to
       validate OpenStack is actually working when deploying with Puppet 3 and 4 versions.
       More details `here <https://github.com/openstack/puppet-openstack-integration#description>`__
     - Yes
     - Read the job logs. Sometimes, the job fails because of
       packaging issues or mirrors downtime. Please report a bug for this so we
       can find workarounds. It can also be a problem in Tempest, a new test
       that is failing or a new parameter which is missing.
   * - gate-tripleo-ci-centos-7-nonha-multinode-nv
     - Deploy a `TripleO <http://docs.openstack.org/developer/tripleo-docs/>`__
       overcloud by running Puppet OpenStack modules.
     - Yes
     - If it's not a TripleO CI downtime, you can dig into
       logs/postci.txt.gz to see why catalog is failing (grep Error).
       Also make sure to consult the `status of TripleO CI <http://tripleo.org/cistatus.html>`__.
   * - puppet-openstack.fuel-library.pkgs.ubuntu.{neutron\_vlan\_ha,smoke\_neutron}
     - Deploy OpenStack cloud on top of libvirt VMs using `Fuel
       <https://wiki.openstack.org/wiki/Fuel>`__ and Puppet OpenStack modules.
       More details `here
       <https://wiki.openstack.org/wiki/Fuel/CI#CI_for_Puppet_OpenStack>`__
     - No
     - You can read the job logs and take a look into diagnostic snapshot
       attached to the build, however it takes some understanding of Fuel
       mechanics to make a good use of this logs. Fuel engineers will
       investigate the failure according to `Fuel CI duty for Puppet OpenStack
       <https://wiki.openstack.org/wiki/Fuel/CI/Puppet_OpenStack_CI_duty>`__
       and may contact you to discuss the reason behind failure. Feel free to
       aks any questions on #fuel-dev at freenode.
   * - puppet-openstack.fuel.noop
     - Read the job logs. Fuel engineers will investigate the failure
       according to `Fuel CI duty for Puppet OpenStack
       <https://wiki.openstack.org/wiki/Fuel/CI/Puppet_OpenStack_CI_duty>`__
       and may contact you to discuss the reason behind failure. Feel free to
       aks any questions on #fuel-dev at freenode.
     - No
     - Run `Fuel-library <https://github.com/openstack/fuel-library>`__ noop
       tests against Puppet OpenStack modules. More details `here
       <http://fuel-noop-fixtures.readthedocs.org/en/latest/>`_
