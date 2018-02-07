`lockss-gitflow-init` is a simple shell script to apply Git settings such
that `gitflow-avh` will use Git Flow layout with the naming and policy
conventions of the LOCKSS Team.

It makes calls to `git config --global` unless `--local` is requested. It
determines whether `gitflow-avh` or similar is installed by calling
`git flow version`.

# Using

Unless you choose to apply local Git settings with `--local`, in which case you
need to run this script in each desired Git tree, you only need to run this
script once, so you only need to download it and run it:

    cd ${INSTALLDIR}
    git clone git@github.com:lockss/lockss-gitflow-init     # with SSH key
    git clone https://github.com/lockss/lockss-gitflow-init # without SSH key
    cd lockss-gitflow-init
    ./lockss-gitflow-init

Other options:

*   `lockss-gitflow-init --help` displays a help message.
*   `lockss-gitflow-init --version` displays the version number.
*   `lockss-gitflow-init --local` stores the Git settings locally
    rather than globally. Must be at the root of a Git tree (as judged by the
    presence of a `.git` directory and `.git/config` file).

# Installing

If you choose to apply Git settings locally to each Git tree rather than
globally with `--local`, you may want to install the script more permanently
in some installation directory `${INSTALLDIR}` (e.g.`${HOME}/software`):

*   Add `${HOME}/bin` to your `$PATH` if it is not already there.

*   Clone from Git:

        cd ${INSTALLDIR}
        git clone git@github.com:lockss/lockss-gitflow-init     # with SSH key
        git clone https://github.com/lockss/lockss-gitflow-init # without SSH key

*   Make a symbolic link:

        cd ${HOME}/bin
        ln -s ${INSTALLDIR}/lockss-gitflow-init/lockss-gitflow-init

## Using

Use the script in a Git tree:

    cd ${MY_GIT_TREE}
    lockss-gitflow-init --local

## Updating

Pull from Git:

    cd ${INSTALLDIR}/lockss-gitflow-init
    git pull
