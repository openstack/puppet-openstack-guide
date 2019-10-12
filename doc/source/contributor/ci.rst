.. _ci:

######################
Continuous Integration
######################


This is a list of the CI jobs that are running against most of the Puppet
OpenStack modules: The code that configures Jenkins jobs is hosted by
`project-config
<http://opendev.org/openstack/project-config/tree/jenkins/jobs/puppet-module-jobs.yaml>`__.

.. list-table:: **CI Jobs in puppet-openstack**
   :widths: 12 25 8 55
   :header-rows: 1

   * - Job name
     - Description
     - Voting
     - What to do in case of failure
   * - puppet-openstack-lint
     - It makes sure the code follows recommended `Puppet style guidelines
       <http://docs.puppetlabs.com/guides/style_guide.html>`__
     - Yes
     - Read the job logs to see where the code does not follow the Puppet lint
       style.
   * - puppet-openstack-syntax-4
     - Syntax checks for Puppet manifests, templates, and Hiera YAML. The jobs
       run on the latest Puppet 4.x release.
     - Yes
     - Read the job logs to see where the code does not follow the Puppet
       syntax style.
   * - puppet-openstack-syntax-5
     - Syntax checks for Puppet manifests, templates, and Hiera YAML. The jobs
       run on the latest Puppet 5.x release.
     - Yes
     - Read the job logs to see where the code does not follow the Puppet
       syntax style.
   * - puppet-openstack-unit-{5.5,6.4}
     - RSpec tests for Puppet manifests on Puppet 5 (for Rocky and earlier) and
       Puppet 6 (for Train and beyond).
     - Yes
     - Read the job logs to see where the tests are failing. `More
       documentation about RSpec <http://rspec-puppet.com/tutorial/>`__
   * - puppet-openstack-unit-latest
     - RSpec tests for Puppet manifests. The jobs run on the latest version
       of Puppet. It aims to be experimental to track any work to do in the
       module to be compatible with the latest release of Puppet.
     - No
     - Read the job logs to see where the tests are failing. Even though the
       job is non-voting, please raise a bug in Launchpad to make sure someone
       has a look and maybe update the module to work with latest version of
       Puppet.
   * - puppet-openstack-beaker-{centos7,xenial}
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
   * - puppet-openstack-integration-4-scenarioX-tempest-{centos7,xenial}
     - Functional testing jobs that will deploy OpenStack run tempest smoke to
       validate OpenStack is actually working when deploying with Puppet 4 on Queens or earlier.
       More details `here <https://github.com/openstack/puppet-openstack-integration#description>`__
     - Yes
     - Read the job logs. Sometimes, the job fails because of
       packaging issues or mirrors downtime. Please report a bug for this so we
       can find workarounds. It can also be a problem in Tempest, a new test
       that is failing or a new parameter which is missing.
   * - puppet-openstack-integration-5-scenarioX-tempest-{centos7,bionic}
     - Functional testing jobs that will deploy OpenStack run tempest smoke to
       validate OpenStack is actually working when deploying with Puppet 5 on Rocky and beyond.
       More details `here <https://github.com/openstack/puppet-openstack-integration#description>`__
     - Yes
     - Read the job logs. Sometimes, the job fails because of
       packaging issues or mirrors downtime. Please report a bug for this so we
       can find workarounds. It can also be a problem in Tempest, a new test
       that is failing or a new parameter which is missing.
