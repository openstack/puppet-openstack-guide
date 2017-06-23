=====================
Starting a new module
=====================

On the community side
=====================

Community wise, one should respect the following process to submit a new
module:

-  Send a message to the mailing-list announcing one's intention to create a
   new puppet module for openstack, and wait for the thread to take place.
-  Once a consensus is reached on the mailing list, the user can
   proceed further by doing two actions:

    #. Submit a review to openstack-infra/project-config to create the
       project (Add PTL and some core as reviewers)
    #. Submit a review to openstack/governance to state that the project is
       part of PuppetOpenstack (Add PTL and some core as reviewers)

For the governance addition please follow the process explained here:
http://docs.openstack.org/infra/manual/creators.html#add-new-repository-to-the-governance-repository

On the technical side
=====================

The community has developed two projects related to modules file
management:

-  puppet-openstack-cookiecutter
   (https://github.com/openstack/puppet-openstack-cookiecutter) : This
   project aims to help bootstrap a new puppet module that will be
   compliant with the community expectations (organization, naming,
   etc...). It takes user inputs and a project template and generate the
   skeleton of the modules.
-  puppet-modulesync-configs
   (https://github.com/openstack/puppet-modulesync-configs) : This
   project aims to gather in a single repository the files that are
   common and need to be kept in sync across all openstack/puppet-\*
   modules.

Why two projects? While modulesync makes it easy to keep a set of common
file synced between projects (Gemfile, Rakefile, nodesets,...), it is
not intended for dynamic content and path (class name, provider,
etc...), hence the use of cookiecutter and the existence of both
projects.

Modulesync: https://github.com/openstack/puppet-modulesync-configs

Cookiecutter: https://github.com/openstack/puppet-openstack-cookiecutter

In practice
===========

Requirements :

-  cookiecutter
-  modulesync (>= 0.6.0)
-  git
-  git-review
-  digest

To make the boilerplating of a new Puppet module easier a script is
provided.
https://github.com/openstack/puppet-openstack-cookiecutter/blob/master/contrib/bootstrap.sh

What it does is the following:

**Step 1: Generate the skeleton of the module**

It uses cookiecutter to generate the skeleton of the module.

**Step 2: Retrieve the git repository of the project**

It retrieves the official openstack repository of your project.

**Step 3: Create the initial commit with the file present in the
skeleton**

Reuse the .git from the openstack repository and make an initial commit
of the files present in the skeleton directory.

**Step 4: Retrieve the puppet-modulesync-configs directory and configure
it for your needs**

It clones the puppet-modulesync-configs directory and configures
modulesync.yml and managed\_modules.yml accordingly.

**Step 5: Run msync and amend the initial commit**

It runs modulesync in noop mode and amends the commit from Step 3 with
the files from puppet-modulesync-configs

At this point you should have generated a minimalist but functional
module.

There are some things that cannot be automated and are marked via the
FIXME tag. The impacted files are:

-  manifests/keystone/auth.pp
-  spec/classes/MYMODULENAME\_keystone\_auth\_spec.rb
-  README.md

**Step 6: Create launchpad project**

See `OpenStack Infra guide <http://docs.openstack.org/infra/manual/creators.html#set-up-launchpad>`_
for setting up launchpad.

Each Puppet module has it own Launchpad project.
The project should be part of "openstack", Driver "hudson-openstack",
Maintainer "puppet-openstack", Bug supervisor "puppet-openstack-bugs".
See https://launchpad.net/puppet-nova for example.


Now you only have to run git review in the folder indicated in the
output of the script.
