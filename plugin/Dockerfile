FROM docker.elastic.co/elasticsearch/elasticsearch:7.6.2

RUN yum -y install epel-release
RUN yum -y install htop
COPY build/distributions/*.zip .
RUN elasticsearch-plugin install -b file:$(ls elastiknn*zip | sort | tail -n1)
