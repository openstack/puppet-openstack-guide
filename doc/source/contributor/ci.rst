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
   * - puppet-openstack-lint-*platform*
     - It makes sure the code follows recommended `Puppet style guidelines
       <http://docs.puppetlabs.com/guides/style_guide.html>`__
     - Yes
     - Read the job logs to see where the code does not follow the Puppet lint
       style.
   * - puppet-openstack-syntax-*N*-*platform*
     - Syntax checks for Puppet manifests, templates, and Hiera YAML. The jobs
       run on the specif Puppet version represented by *N*.
     - Yes
     - Read the job logs to see where the code does not follow the Puppet
       syntax style.
   * - puppet-openstack-unit-*N*-*platform*
     - RSpec tests for Puppet manifests. *N* represents version of Puppet used
       in the test.
     - Yes
     - Read the job logs to see where the tests are failing. `More
       documentation about RSpec <http://rspec-puppet.com/tutorial/>`__
   * - puppet-openstack-unit-latest-*platform*
     - RSpec tests for Puppet manifests. The jobs run on the latest version
       of Puppet. It aims to be experimental to track any work to do in the
       module to be compatible with the latest release of Puppet.
     - No
     - Read the job logs to see where the tests are failing. Even though the
       job is non-voting, please raise a bug in Launchpad to make sure someone
       has a look and maybe update the module to work with latest version of
       Puppet.
   * - puppet-openstack-litmus-*N*-*platform*
     - Litmus jobs to do functional testing. It will prepare the Puppet
       environment on 2 different systems (CentOS and Ubuntu), run
       Puppet to configure the module resources and run some tests with
       serverspec.
     - Yes
     - Read the job logs. Sometimes, the job fails because of packaging issues
       or mirrors downtime. Please report a bug for this so we can find
       workarounds. Otherwise, make sure your patch is supposed to work with
       current tests or you'll have to adapt the tests to change the expected
       behavior. `More documentation about Litmus
       <https://puppetlabs.github.io/litmus/>`__
   * - puppet-openstack-integration-*N*-scenarioX-tempest-*platform*
     - Functional testing jobs that will deploy OpenStack run tempest smoke to
       validate OpenStack is actually working. *N* represents the Puppet version
       used in the test.
       More details `here <https://opendev.org/openstack/puppet-openstack-integration#description>`__
     - Yes
     - Read the job logs. Sometimes, the job fails because of
       packaging issues or mirrors downtime. Please report a bug for this so we
       can find workarounds. It can also be a problem in Tempest, a new test
       that is failing or a new parameter which is missing.
       To find some more tips to troubleshoot failures of these jobs, check
       the below section.


Definition of base jobs is maintained in `puppet-openstack-integration <https://opendev.org/openstack/puppet-openstack-integration>`__.
From Rocky release, the job definition is described in the yaml files under the
`zuul.d <https://opendev.org/openstack/puppet-openstack-integration/src/branch/master/zuul.d>`__
directry. Each module has its own .zuul.yaml file and define a list of jobs
executed against any change in that repo.


Troubleshooting Integration Tests
---------------------------------

When any integration jon fails, the following items in zuul build log help you
identify the cause of failures.

- Log files for each service is stored in the ``logs/<service name>`` directory.

- Output of some diagnostic commands like ``ps`` is also stoed in the ``logs``
  directory.

- Configuration files are stored under the ``logs/etc`` directory. You can
  check each configuration file to see how parameters are set.

- Output of puppet execution is recorded in ``logs/puppet*.txt``. Because
  we execute puppet 2 times to ensure idempotency, two files are created
  unless the first run fails.

- Tempest output is logged in ``job-outputs.txt``. The report file is created
  as ``logs/testr_results.html`` .

The `copy_logs.sh <https://opendev.org/openstack/puppet-openstack-integration/src/branch/master/copy_logs.sh>`__
script is used to capture log files during CI tests. Please propose any additional
items you think are useful.
