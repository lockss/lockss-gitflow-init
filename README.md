`lockss-gitflow-init` is a simple shell script to apply Git settings such
that `gitflow-avh` will use Git Flow layout with the naming and policy
conventions of the LOCKSS Team.

It makes calls to `git config --global` unless `--local` is requested. It
determines whether `gitflow-avh` or similar is installed by calling
`git flow version`.

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

* Run `lockss-gitflow-init`

* Other options:

    * `lockss-gitflow-init --help` displays a help message.
    * `lockss-gitflow-init --version` displays the version number.
    * `lockss-gitflow-init --local` stores the Git settings locally
       rather than globally.

# Updating

* Pull from Git:

        cd ${INSTALLDIR}/lockss-gitflow-init
        git pull
