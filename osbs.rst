.. _osbs:

++++
OSBS
++++

Fedora's Openshift Build System
===============================

Upstream
********

* `atomic-reactor <https://github.com/projectatomic/atomic-reactor>`_
* `osbs-client <https://github.com/projectatomic/osbs-client>`_
* `Openshift (Build system) <https://docs.openshift.org/latest/dev_guide/builds.html>`_
* `koji-containerbuild <https://github.com/release-engineering/koji-containerbuild>`_

Documentation
*************

* `osbs doc <https://github.com/projectatomic/osbs-docs>`_ and on `readthedocs <https://readthedocs.org/projects/osbs/>`_
* `Fedora Layered Image Build System <https://docs.pagure.org/releng/layered_image_build_service.html>`_

 
Deployment
**********

Fedora Infrastructure ansible: 

* `osbs cluster playbook <https://infrastructure.fedoraproject.org/cgit/ansible.git/tree/playbooks/groups/osbs-cluster.yml>`_
* `osbs atomic-reactor role <https://infrastructure.fedoraproject.org/cgit/ansible.git/tree/roles/osbs-atomic-reactor>`_
* `osbs-client role <https://infrastructure.fedoraproject.org/cgit/ansible.git/tree/roles/osbs-client>`_
* `osbs-common <https://infrastructure.fedoraproject.org/cgit/ansible.git/tree/roles/osbs-common>`_
* `osbs-namespace <https://infrastructure.fedoraproject.org/cgit/ansible.git/tree/roles/osbs-namespace>`_
* `osbs-on-openshift <https://infrastructure.fedoraproject.org/cgit/ansible.git/tree/roles/osbs-on-openshift>`_
* `ansible-ansible-openshift-ansible role <https://infrastructure.fedoraproject.org/cgit/ansible.git/tree/roles/ansible-ansible-openshift-ansible>`_

Fedora Infrastructure SOP:

* `FLIBS SOP <https://fedora-infra-docs.readthedocs.io/en/latest/sysadmin-guide/sops/layered-image-buildsys.html>`_

Packages
********

* https://src.fedoraproject.org/rpms/osbs-client
* https://src.fedoraproject.org/rpms/atomic-reactor
* https://src.fedoraproject.org/rpms/koji-containerbuild



Misc
****

`historical bugzilla FLIBS <https://bugzilla.redhat.com/show_bug.cgi?id=1243736>`_
