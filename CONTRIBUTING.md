# Git Layout

This Git repository uses the LOCKSS naming and policy conventions for Git Flow,
which are:

* The stable and development branches are `master` and `develop` respectively.
* The prefixes for feature, release and hotfix branches are `feature-`,
  `release-` and `hotfix-` respectively.
* The prefixes for support and bugfix branches are `support-` and `bugfix-`
  respectively (but we do not use them).
* The prefix for release tags is `version-`
* Set configuration parameters such that finishing a feature, release or hotfix
  squashes during merge and keeps both the local and remote branches.

Resources:

* https://github.com/petervanderdoes/gitflow-avh
* https://danielkummer.github.io/git-flow-cheatsheet/
* https://github.com/lockss/lockss-gitflow-init