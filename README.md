rkt install playbook
====================

This playbook is tested with CentOS7.
But it should be work with other RHEL7 comparible distribution.

Install rkt
-----------

Just run site.yml with ansible:

    # ansible-playbook site.yml

If you want to install remote host, prepare inventory file.

Run Container
-------------

Example to run centos docker image on rkt:

    # rkt --insecure-options=image fetch docker://centos
    # rkt --insecure-options=image run registry-1.docker.io/library/centos  --interactive --exec=/bin/sh