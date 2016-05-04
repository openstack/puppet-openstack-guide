*******
Reviews
*******

1. `Review policy`_
2. `Abandonment`_


Review policy
=============

Code is merged based on the voting process of the modules in Gerrit. All
submitted patches automatically trigger a job that runs its rspec-puppet
tests. This job is considered to be a gate in that no code is allowed to be
merged that does not pass these tests. The results of this job are listed for
every patch as a +1 Verified vote from Jenkis.

Any users can +/- 1 a commit and add comments on commit, but only members of
the puppet-manager-core group have the ability to +2 and approve code to be
merged.



Abandonment
===========

If a change is submitted and given a -1, and subsequently the author becomes
unresponsive for a few weeks, reviewers should leave reminder comments on the
review or attempt to contact the original author via IRC or email. If the
change is easy to fix, anyone should feel welcome to check out the change and
resubmit it using the same change ID to preserve original authorship. Core
reviewers will not abandon such a change.

If a change is submitted and given a -2, or it otherwise becomes clear that
the change can not make it in (for example, if an alternate change was chosen
to solve the problem), and the author has been unresponsive for at least 3
months, a core reviewer should abandon the change.

This policy is subject to change as we review our bandwidth for taking up
forgotten patches and monitor our backlog growth.

