FROM fedora23_maj
MAINTAINER hme 

RUN yum -y install wget tar git
RUN yum -y install java-1.8.0-openjdk-headless.x86_64

RUN mkdir -p /home/jmeter

WORKDIR /home/jmeter
RUN wget http://wwwftp.ciril.fr/pub/apache/jmeter/binaries/apache-jmeter-3.1.tgz

RUN mkdir -p /home/developpement

RUN git clone https://github.com/astondevops/web_server_flask.git

