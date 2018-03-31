# Build docker tomcat image
It will detect and download latest 8.0.x Apache Tomcat, extracts it to /opt/tomcat
Installs openjdk8-jre
tomcat will start under **tomcat** user not root

1. Get the file
2. run: docker build -f Dockerfile . -t mytomcat:latest
3. run: docker run -d -p 8080:8080 mytomcat:latest
   or:  docker run -d -p 8080:8080 -v /my/own/webapps:/opt/tomcat/webapps mytomcat:latest 'and then drop your war into /my/own/webapps folder
4. enjoy
