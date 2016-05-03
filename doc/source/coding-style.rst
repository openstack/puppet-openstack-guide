Coding Style
------------

.. note:: this document is work in progress and the content with evolve. Any
          contribution is welcome though ;-)

-  Read this page
-  Make sure that what you're going to code is not already work in
   progress
-  Make sure you're familiar with Puppet Syntax,
   `Lint <http://puppet-lint.com/>`__,
   `Rspec <http://rspec-puppet.com/>`__, and
   `Beaker <https://github.com/puppetlabs/beaker>`__
-  If you want to create a new module, read
   `New\_module <http://docs.openstack.org/developer/puppet-openstack-guide/new-module.html>`__

Best practices
--------------

Deprecation
~~~~~~~~~~~

Any patch **must be** backward compatible.

It meansː

-  do not break the interface (deprecate parameters for at least one
   cycle, and add a warning for our users)
-  do not change default parameters (except if you have a good reason
   but your commit message must explain it)

Commit message
~~~~~~~~~~~~~~

Please read `GitCommitMessages <GitCommitMessages>`__.

Consistency
~~~~~~~~~~~

We have a lot of modules to maintain, please keep our code consistent.
Before adding new parameters or new classes, see if other modules
already implement them and keep consistent. See also our common libraries
`OpenStackLib <http://git.openstack.org/cgit/openstack/puppet-openstacklib/>`__

Config file defaults and parameters
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~

We want users that don't override a value to get the default for the
service being configured. Many of the parameters passed in to classes
and defined types translate directly into a config file setting. When a
parameter translates directly to a config file value, and the value is
optional, it should be set to ``$::os_service_default``. This is a
special value that will ensure that the service default is used by
removing any existing value from the config file.

Empty parameters
~~~~~~~~~~~~~~~~

When you need to specify a empty (nil) parameter, using
`undef <https://docs.puppetlabs.com/puppet/latest/reference/lang_data_undef.html>`__
is the best choice. Do not useː " (not Puppetish) or false (undef is
false if tested as a boolean).

Testing
-------

Testing is required for all new code. Puppet OpenStack CI will
`verify <http://docs.openstack.org/developer/puppet-openstack-guide/ci.html>`__
your changes, but to save time it is better to run tests locally before
submitting the patch.

-  `Lint <http://puppet-lint.com/>`__
-  `Syntax <https://puppetlabs.com/blog/verifying-puppet-checking-syntax-and-writing-automated-tests>`__
-  `Testing <http://docs.openstack.org/developer/puppet-openstack-guide/testing.html>`__

Documentation
-------------

-  Validate all parameters are documented. They are required and lint
   will check it.
-  If possible, keep examples/\*.pp updated, they are very useful for
   our users.
-  Comment your code when needed (temporary workarounds, TODO, etc).

Asking for review
-----------------

Different ways to get reviewsː

-  Go on IRC ``#puppet-openstack`` (freenode) and gently ask for
   reviews. If you need to discuss about already reviewed code, you can
   ping the reviewers.
-  Add your patch on the `Puppet OpenStack meeting
   Agenda <http://docs.openstack.org/developer/puppet-openstack-guide/meetings.html>`__ (in Open Discussion
   section).
-  Use `Mailing list <http://docs.openstack.org/developer/puppet-openstack-guide/mailing-list.html>`__.
