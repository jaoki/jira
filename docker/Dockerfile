FROM centos:centos7

RUN yum install -y wget vim tar unzip

RUN cd /usr/local/lib && wget https://bobswift.atlassian.net/wiki/download/attachments/16285777/atlassian-cli-4.5.0-distribution.zip
RUN cd /usr/local/lib && unzip atlassian-cli-4.5.0-distribution.zip 

ENV JIRA_HOME /usr/local/lib/atlassian-cli-4.5.0
ENV PATH $JIRA_HOME:$PATH


RUN cd /usr/local/lib && wget --no-cookies --no-check-certificate --header "Cookie: gpw_e24=http%3A%2F%2Fwww.oracle.com%2F; oraclelicense=accept-securebackup-cookie" "http://download.oracle.com/otn-pub/java/jdk/8u51-b16/jdk-8u51-linux-x64.tar.gz" 
RUN cd /usr/local/lib && tar xf jdk-8u51-linux-x64.tar.gz

ENV JAVA_HOME /usr/local/lib/jdk1.8.0_51
ENV PATH $PATH:$JAVA_HOME/bin

RUN chmod og+x -R $JIRA_HOME

RUN cd /usr/local/lib && rm atlassian-cli-4.5.0-distribution.zip && rm jdk-8u51-linux-x64.tar.gz 

