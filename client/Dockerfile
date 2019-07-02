FROM nginx:1.17.1
LABEL maintainer="Steve S Gee Jr <steve.gee@sprint.com>"
LABEL version="1.0.0"
WORKDIR /


RUN echo "deb [check-valid-until=no] http://cdn-fastly.deb.debian.org/debian jessie main" > /etc/apt/sources.list.d/jessie.list
RUN echo "deb [check-valid-until=no] http://archive.debian.org/debian jessie-backports main" > /etc/apt/sources.list.d/jessie-backports.list
RUN sed -i '/deb http:\/\/deb.debian.org\/debian jessie-updates main/d' /etc/apt/sources.list
RUN apt-get -o Acquire::Check-Valid-Until=false update
RUN apt-get install -y curl wget telnet iputils-ping vim


#RUN apt-get update && apt-get install -y \
  #curl \
  #wget \
  #ping \
  #telnet \
  #&& rm -rf /var/lib/apt/lists/*
