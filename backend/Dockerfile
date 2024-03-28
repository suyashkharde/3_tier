FROM centos:7
USER root
RUN mkdir /opt/tomcat/
WORKDIR /opt/tomcat
ADD https://dlcdn.apache.org/tomcat/tomcat-9/v9.0.87/bin/apache-tomcat-9.0.87.tar.gz /opt/tomcat
RUN tar -xzvf apache-tomcat-9.0.87.tar.gz
RUN yum install java -y
WORKDIR /opt/tomcat/apache-tomcat-9.0.87/
COPY student.war webapps/student.war
COPY context.xml conf/context.xml
ADD https://s3-us-west-2.amazonaws.com/studentapi-cit/mysql-connector.jar /lib/mysql-connector.jar
EXPOSE 8080
CMD [ "/opt/tomcat/bin/catalina.sh", "run" ]
