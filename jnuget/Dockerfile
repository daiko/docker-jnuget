FROM tomcat:9-jre9

RUN mkdir -p /var/lib/jnuget/Packages \
 && rm -rf /usr/local/tomcat/webapps/ROOT

RUN cd /usr/local/tomcat/webapps/ \
	&& wget -O ROOT.war https://bitbucket.org/aristar/jnuget/downloads/jnuget-server-0.8.4.1-SNAPSHOT.war

#COPY ./config/jnuget.config.xml /var/lib/jnuget/jnuget.config.xml
#COPY ./config/jnuget.users.xml /var/lib/jnuget/jnuget.users.xml

ENV NUGET_HOME /var/lib/jnuget

EXPOSE 8080

VOLUME ["/var/lib/jnuget","/usr/local/tomcat/logs","/usr/local/tomcat/conf"]
