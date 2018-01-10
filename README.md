`lockss-gitflow-init` is a simple shell script to initialize a Git repository
so that it uses Git Flow with the naming conventions of the LOCKSS Team.

It makes calls to `git config --local`, then calls
`git flow init --local --defaults` to create branches. It determines whether
`gitflow-avh` or similar is installed by calling `git flow version`.

This repository uses, and this script implements, the LOCKSS conventions for Git
Flow, which are:

* The stable branch is `master`
* The development branch is `develop`
* The prefix for feature branches is `feature-`
* The prefix for release branches is `release-`
* The prefix for hotfix branches is `hotfix-`
* The prefix for support branches is `support-` (but we do not use them)
* The prefix for release tags is `version-`

# Installing

Recommended setup for some installation directory `${INSTALLDIR}` (e.g.
`${HOME}/software`):

* Add `${HOME}/bin` to your `$PATH`.

* Clone from Git:

        cd ${INSTALLDIR}
        git clone git@github.com:lockss/lockss-gitflow-init     # with SSH key
        git clone https://github.com/lockss/lockss-gitflow-init # without SSH key

* Make a symbolic link:

        cd ${HOME}/bin
        ln -s ${INSTALLDIR}/lockss-gitflow-init/lockss-gitflow-init

# Using

* At the root of a Git repository, invoke `lockss-gitflow-init`.
* It fails if it cannot find a `.git` directory or if invoking
  `git flow version` fails.
* It outputs progress messages to standard output.
* Other options:
    * `lockss-gitflow-init --help` displays a help message.
    * `lockss-gitflow-init --version` displays the version number.

# Updating

* Pull from Git:

        cd ${INSTALLDIR}/lockss-gitflow-init
        git pull
