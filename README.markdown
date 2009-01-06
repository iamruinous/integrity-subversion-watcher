Integrity Subversion Watcher
============================

Integrity Subversion Watcher is a fun companion to your friendly automated Continuous Integration server.

Its purpose is to check for updates to your subversion repository, then trigger a build if a new revision is available.

Getting Started
===============

Make sure the `iamruinous-integrity` gem is installed from GitHub:

    gem sources --add http://gems.github.com
    sudo gem install iamruinous-integrity

Then checkout the `integrity-subversion-watcher` project:

    git clone git://github.com/iamruinous/integrity-subversion-watcher.git

Run the watcher and trigger a build (you must also specify the location of the integrity configuration file):

    ruby integrity-subversion-watcher check "project1,project2" --config=/path/to/config.yml

If the script detects a newer revision in your subversion repository, it will cause Integrity to build your project