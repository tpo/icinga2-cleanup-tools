icinga2-cleanup-tools
=====================

If you make a mess with your icinga2 installation
and you want to clean up icingas state, then
what you can do is to remove the various state files
and drop the DB, and recreate it after.

Keep in mind, that the icinga2 nodes that are
connecting and reporting to the icinga2 master do
have their own state too, which you'll possibly
want to delete as well.

### WARNING

These tools are *HACKS*! They

    # rm /some/path/\*
    # dropdb icinga

stuff, so you better be sure you really want to loose
these data! They should give you an idea how to clean
up, and thus are meant as an inspiration.

You should *NOT* use them blindly! Have a look at them
before using them and adapt them first to your own
setup and paths.

They have been tested on Debian wheezy with the debmon
repository.

### Tools description

#### icinga-cmd

Send commands to icinga. I've used it like this:

    # icinga-cmd "DISABLE_NOTIFICATIONS"

#### make-icinga-state-backup

Backups the icinga state but *NOT* the DB. Adapt to
your needs!

#### remove-icinga-state

Removes icinga state and *DROPS* the DB. *You need
to adapt this to your needs!*

### LICENSE

### Author and Contact
Tomas Pospise <tpo_deb@sourcepole.ch>
