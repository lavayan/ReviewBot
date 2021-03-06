.. _upgrading:

=========
Upgrading
=========

Upgrading from Review Bot 1.0+
==============================

Upgrading Review Bot is easy. To start, upgrade the extension on the Review
Board server::

    $ sudo pip install -U reviewbot-extension

And then upgrade each worker::

    $ sudo pip install -U reviewbot-worker

(If you're installing in a virtual environment, don't use ``sudo``.)

Depending on your configuration, you may need to restart or reload your web
server. The specific command depends on your individual setup, but is usually
something like the following::

    $ sudo service httpd reload

Open the Review Board administration page and click :guilabel:`Extensions`.
You should see the new version of Review Bot installed.


Upgrading from Review Bot 0.1 or 0.2
====================================

The configuration of Review Bot 0.1 and 0.2 worked differently than modern
versions, so to start, make a note of all your settings.

Then you'll need to uninstall the old extension on the Review Board server::

    $ sudo pip uninstall Review_Bot_Extension

And then uninstall each worker::

    $ sudo pip uninstall ReviewBot

Then follow the :ref:`installation instructions <installation>` to install a
modern version.
