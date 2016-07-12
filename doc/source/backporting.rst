Backporting
===========

This page documents the Puppet OpenStack backport policy.

Can be backported
-----------------

-  Critical and High bugs fixes, if reported in Launchpad.
-  Features if they don't change anything in the stable interface and
   only if backward compatibility is fully respected. Also if the
   feature works for the OpenStack release where it's backported to.

Cannot be backported
--------------------

-  Medium and Low bug fixes
-  Features that break backward compatibility or change the existing
   interface (default values or name of parameters).

Merge Conflict
--------------

-  Explain in commit message what is conflicting and how it's resolved.
-  Document the changes between master and stable branches in the code
   or in the commit message.
