.. _osbs:

++++++++++
OSBS notes
++++++++++

Fedora's Openshift Build System
===============================

Upstream
********

* `atomic-reactor <https://github.com/projectatomic/atomic-reactor>`_
* `osbs-client <https://github.com/projectatomic/osbs-client>`_
* `Openshift (Build system) <https://docs.openshift.org/latest/dev_guide/builds.html>`_
* `koji-containerbuild <https://github.com/release-engineering/koji-containerbuild>`_

Development Environment

* `osbs-box <https://github.com/lcarva/osbs-box>`_


Documentation
*************

* `osbs doc <https://github.com/projectatomic/osbs-docs>`_ and on `readthedocs <https://readthedocs.org/projects/osbs/>`_
* `Fedora Layered Image Build System <https://docs.pagure.org/releng/layered_image_build_service.html>`_
* `OSBS deployment guide <https://github.com/projectatomic/osbs-client/blob/master/docs/osbs_instance_setup.md>`_

 
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

Rebuild of container buildroot ::

    $ docker build -t buildroot --rm --no-cache /etc/osbs/buildroot

Update packages on target using ansible ::

    $ ansible $target -m package -a "name=koji-containerbuild state=latest"

Check for build running in openshift ::

    $ oc login
    $ oc status
    $ oc -n osbs-fedora describe build <my-build>

Get builds for a namespace ::

    $ oc -n namespace get build

Cancel a build ::

    $ oc -n namespace cancel-build <my-build>

Docker insecure-registry : To add the insecure registry need to edit the /etc/sysconfig/docker and modify the OPTIONS parameter

`historical bugzilla FLIBS <https://bugzilla.redhat.com/show_bug.cgi?id=1243736>`_
