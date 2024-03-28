FROM centos:7
USER root
WORKDIR /opt/
ADD https://dlcdn.apache.org/tomcat/tomcat-9/v9.0.87/bin/apache-tomcat-9.0.87.tar.gz .
RUN tar -xzvf apache-tomcat-9.0.87.tar.gz -C /opt/
RUN yum install java -y
WORKDIR /opt/apache-tomcat-9.0.87
COPY student.war webapps/student.war
COPY context.xml conf/context.xml
ADD https://s3-us-west-2.amazonaws.com/studentapi-cit/mysql-connector.jar lib/mysql-connector.jar
EXPOSE 8080
CMD [ "bin/catalina.sh", "run" ]

