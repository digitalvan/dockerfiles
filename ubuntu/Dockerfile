FROM digitalvan/ubuntu:latest-perl-deps

RUN apt-get update -y
RUN apt-get install -y make gcc wget

RUN  wget http://www.cpan.org/src/5.0/perl-5.26.1.tar.gz; \
     tar -xzf perl-5.26.1.tar.gz; \
     cd perl-5.26.1; \
     ./Configure -des -Dprefix=$HOME/localperl; \
     make; \
     make test; \
     make install; \

