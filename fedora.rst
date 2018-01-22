.. _fedora:

++++++
Fedora
++++++

Fedora notes
============

Disk usage ::

    $ du -shxc /*

-s = summarize

-h = human readable

-x = one file system

-c = grant total


Koji scratch build ::

    $ koji build --scratch f27 package.srpm

Curl download of file ::

    $ curl -o name_of_the_file https://url_of _the_file
