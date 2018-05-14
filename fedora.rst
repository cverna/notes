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

Build a srpm with mock ::

    $ mock -v -r fedora-27-x86_64 SPRM/my.sprm

RPM get version of an rpm ::

    $ rpm -q --qf "%{version}\n" python3

journalctl follow a service logs ::

   $ journalctl -lfu name_of_the_service


NEOVIM
======

Using cscope with for Python.
First need to install the pycscope project https://github.com/portante/pycscope.
Then generate the cscope output file ::

    $ cd source_code_dir
    $ pycscope -R

This generate a cscope.out file. Inside vim run the following command to add the cscope file to the db ::

    :cs add cscope.out

Then use the cs command to search the symbols ::

    find = Query cscope.  All cscope query options are available 
    except option #5 ("Change this grep pattern").

    USAGE = cs find {querytype} {name}

    {querytype} corresponds to the actual cscope line
    
    interface numbers as well as default nvi commands:

    0 or s: Find this C symbol
    1 or g: Find this definition
    2 or d: Find functions called by this function
    3 or c: Find functions calling this function
    4 or t: Find this text string
    6 or e: Find this egrep pattern
    7 or f: Find this file
    8 or i: Find files #including this file
    9 or a: Find places where this symbol is assigned a value
