FROM centos:7
LABEL app="Studentapp"
USER root
WORKDIR /opt/
ADD https://dlcdn.apache.org/tomcat/tomcat-9/v9.0.87/bin/apache-tomcat-9.0.87.tar.gz .
RUN tar -xzvf apache-tomcat-9.0.87.tar.gz
RUN yum install java -y
WORKDIR /apache-tomcat-9.0.87
COPY student.war webapps/
ADD https://s3-us-west-2.amazonaws.com/studentapi-cit/mysql-connector.jar /apache-tomcat-9.0.87/lib
EXPOSE 8080
CMD [ "catalina.sh", "RUN" ]
