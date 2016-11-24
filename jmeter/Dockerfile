FROM fedora23_maj
MAINTAINER hme 

RUN yum -y install wget tar git python3
RUN yum -y install java-1.8.0-openjdk-headless.x86_64

RUN mkdir -p /home/jmeter

WORKDIR /home/jmeter
RUN wget http://wwwftp.ciril.fr/pub/apache/jmeter/binaries/apache-jmeter-3.1.tgz
RUN tar -zxvf apache-jmeter-3.1.tgz

RUN mkdir -p /home/developpement
WORKDIR /home/developpement
RUN git clone https://github.com/astondevops/web_server_flask.git

VOLUME ['/jmeter_log']

WORKDIR /home/jmeter/apache-jmeter-3.1/bin
#ENTRYPOINT ['jmeter']
#:CMD ['-?']
WORKDIR /home/developpement/web_server_flask/jmeter_jmx
CMD ["jmeter_ligne_command.sh"]
