.. _coding_style:

============
Coding Style
============

.. note:: this document is a work in progress and the content will evolve. Any contribution is welcome though ;-)

- Read this page
- Make sure that what you're going to code is not already a work in
  progress
- Make sure you're familiar with Puppet Syntax, Lint_, Rspec_ and Litmus_
- If you want to create a new module, read `New Module <new-module.html>`_.

.. _Lint: http://puppet-lint.com/
.. _Rspec: http://rspec-puppet.com/
.. _Litmus: https://puppetlabs.github.io/litmus/


Best practices
==============

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

Please read GitCommitMessages_

.. _GitCommitMessages: https://wiki.openstack.org/wiki/GitCommitMessages

Consistency
~~~~~~~~~~~

We have a lot of modules to maintain, please keep our code consistent.
Before adding new parameters or new classes, see if other modules
already implement them and keep consistent. See also our common libraries
`OpenStackLib <http://opendev.org/openstack/puppet-openstacklib/>`__

Class structure and dependencies
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~

The structure of classes should be consistent between modules for common resources.
There should be as few include or require statements as possible unless absolutely
neccesary, such as in the case when backward compatibility is required.

This helps to prevent redeclaration problems and issues where consumers of the modules
are forced to place resources in the proper order in their manifests to not cause those
issues. We should strive towards not enforcing ordering of resources in code, if we have
to do that we should inform our users properly and fail early unless the condition is met.

Note that this is not about the runtime dependency chain of resources but about placement
of code that can cause redeclaration issues because we include a class in another and the
consumer specifying that class at the same time.

Classes should be used to logically split up the functionality of modules to not
place everything in the same place. For example in the ``puppet-cinder`` instead
of having ``cinder::nova_username`` which configures ``[nova]/username`` you should
instead supply the ``cinder::nova`` class that takes care of the whole ``nova`` config
section.

Same structure should be used for database, logging etc to not group up all the
configuration options in the init class of the modules. Examples of this is the
``<modules>::db```and ``<module>::logging`` classes we have today.

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

When you need to specify an empty (nil) parameter, using
`undef <https://docs.puppetlabs.com/puppet/latest/reference/lang_data_undef.html>`__
is the best choice. Do not useː " (not Puppetish) or false (undef is
false if tested as a boolean).

Adding new depdnency
~~~~~~~~~~~~~~~~~~~~

When you add a new dependency, update ``metadata.json`` in that repository.
If the new dependency is not yet used by the other modules, then that should be added to
`Puppetfile <https://opendev.org/openstack/puppet-openstack-integration/src/branch/master/Puppetfile>`__
so that the new dependency is installed during tests.
If the new depdnency is already used in the other modules, then set the consistent
version constraints unless you have a specific requirement,


Testing
=======

Everything about testing you can find `here <testing.html>`_.

Documentation
=============

-  Validate all parameters are documented. They are required and lint
   will check it.
-  If possible, keep examples/\*.pp updated, they are very useful for
   our users.
-  Comment your code when needed (temporary workarounds, TODO, etc).
-  Any change in interface (like new parameters, deprecations, and etc) or
   fundamental behavior should be documented in a release note. In Puppet OpenStack,
   we use `reno <https://docs.openstack.org/reno/latest/>`__ to maintain release notes.
