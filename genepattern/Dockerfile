#
# GenePattern Server Image
# Version 0.1
#
FROM ubuntu:14.04
#
MAINTAINER Chris Norman "cnorman@broadinstitute.org"
#
# Install Java 8 JDK
#
RUN \
  echo oracle-java8-installer shared/accepted-oracle-license-v1-1 select true | debconf-set-selections && \
  apt-get -q -y install software-properties-common && \
  add-apt-repository -y ppa:webupd8team/java && \
  apt-get update && \
  apt-get install -y oracle-java8-installer
ENV JAVA_HOME /usr/lib/jvm/java-8-oracle
#
# Define a workdir for subsequent RUN, CMD and ENTRYPOINT instructions
#
# WORKDIR /data
#
#
# Install (current) version of R 
#
RUN apt-get install -y --no-install-recommends \
    r-base r-base-dev r-recommended
#
# Install GenePattern
#
# [RUN cmd here]
#
# Expose port 8080
#
EXPOSE 8080

