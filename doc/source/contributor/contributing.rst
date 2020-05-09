============================
So You Want to Contribute...
============================

For general information on contributing to OpenStack, please check out the
`contributor guide <https://docs.openstack.org/contributors/>`_ to get started.
It covers all the basics that are common to all OpenStack projects: the accounts
you need, the basics of interacting with our Gerrit review system, how we
communicate as a community, etc.

The Puppet OpenStack team manages a lot of OpenStack related Puppet modules for
consumation by deployers, below topics covers Puppet OpenStack specific contribution
standards.

.. toctree::
   :titlesonly:
   :maxdepth: 1

   coding-style
   testing
   new-module
   backporting
   reviews

Communication
~~~~~~~~~~~~~
* If you have something to discuss use
  `OpenStack discuss mail-list <http://lists.openstack.org/cgi-bin/mailman/listinfo/openstack-discuss>`_.
  Prefix the mail subject with ``[puppet]``

* Join ``#puppet-openstack`` IRC channel on `freenode <http://freenode.net/>`_

Contacting the Core Team
~~~~~~~~~~~~~~~~~~~~~~~~

* The core team has coverage in multiple timezones.

* Just pop over to IRC; we keep a close eye on it!

* You can also find the email addresses of the core team `here <https://review.opendev.org/#/admin/groups/134,members>`_.

Some modules have sub-groups with more cores that help maintain specific modules.

New Feature Planning
~~~~~~~~~~~~~~~~~~~~
Puppet OpenStack uses specs to track major feature requests but does not
require it for smaller changes. Specs follow a defined format and are
submitted as change requests to the openstack/puppet-openstack-specs
repository.

Reporting a Bug
~~~~~~~~~~~~~~~
We currently use Launchpad to track bugs per Puppet module, because of
limited resources we do no longer perform triage, please let us know on
IRC or to core members to raise our attention.

Getting Your Patch Merged
~~~~~~~~~~~~~~~~~~~~~~~~~
Typically two +2s are required before merging.

Project Team Lead Duties
~~~~~~~~~~~~~~~~~~~~~~~~
If you are the PTL of Puppet OpenStack then you should follow the `PTL guide
<https://docs.openstack.org/project-team-guide/ptl.html>`_.
