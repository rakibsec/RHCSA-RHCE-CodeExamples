
Run docker container with centos 7
----------------------------------

    docker-machine rm dev
    docker-machine create -d virtualbox dev
    eval $(docker-machine env dev )
    docker run -it centos:7 bash

Enable documentation
--------------------

    yum install nano
    nano /etc/yum.conf >>
      # tsflags=nodocs
    yum install man
    yum reinstall nano
    man nano

or

    which useradd
    yum install man
    rpm -q -f /usr/sbin/useradd
    yumdownloader shadow-utils
    rpm --upgrade --force  shadow-utils-4.1.5.1-18.el7.x86_64.rpm
