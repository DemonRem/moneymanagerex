FROM centos:7
MAINTAINER developers@moneymanagerex.org
RUN rpm --import https://getfedora.org/static/352C64E5.txt \
 && yum -y install http://download.fedoraproject.org/pub/epel/epel-release-latest-7.noarch.rpm \
 && yum -y install --setopt=tsflags=nodocs \
        cmake3 gcc-c++ gettext git make rpm-build redhat-lsb-core \
        webkitgtk3-devel wxGTK3-devel \
        automake libtool ccache \
 && yum clean all

# cmake3 installed from EPEL
RUN for f in cmake make pack test; do \
      ln -sv /usr/bin/c${f}3 /usr/bin/c${f}; done
