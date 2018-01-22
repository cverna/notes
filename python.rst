.. _python:

++++++
Python
++++++

Python Trick and Tips
=====================

Get a dict keys in a for loop ::

  a = {'a': 1, 'b': 2, 'c': 3}
  for key in a:
    print(key)

the keys a, b and c will be printed.

Run a single test with nose ::

  nosetests name_of_the_module.py:Nameoftheclass.nameofthetest

Get Color in a container shell ::

  docker exec -it -e TERM=xterm name_of_container /bin/bash

Usefull debugger ipdb ::

  $ dnf install python2-ipdb
