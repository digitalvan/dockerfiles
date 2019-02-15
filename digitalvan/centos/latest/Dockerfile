FROM centos:latest

RUN yum update -y 
RUN yum install -y ant cloc cmake curl-devel cvs dvi2ps git git-contrib \
    git-subtree latex libcurl-devel perl perl-ExtUtils perl-Mk ps2pdf python python-devel \ 
    python-doc python-docutils R sloc svn tcl tetex tetex-fonts tetex-dvips tetex-latex ghostscript \ 
    texlive tree wget xz zlib-devel
RUN useradd -ms /bin/bash jenkins

COPY terraform /usr/local/bin 
COPY jre-8u5-linux-x64.rpm /tmp
RUN rpm -Uvh /tmp/jre-8u5-linux-x64.rpm && rm -f /tmp/jre-8u5-linux-x64.rpm

USER jenkins
WORKDIR /home/jenkins
