FROM amazonlinux:2023
RUN yum update 
WORKDIR APP
RUN yum install wget -y
RUN mkdir -p /usr/share/man/man1/
RUN wget https://download.java.net/java/GA/jdk17/0d483333a00540d886896bac774ff48b/35/GPL/openjdk-17_linux-x64_bin.tar.gz
RUN yum install tar -y
RUN yum install gzip -y
RUN tar xvf openjdk-17_linux-x64_bin.tar.gz

# Setup JAVA_HOME 
ENV JAVA_HOME /usr/lib/jvm/openjdk-17
ENV JAVA_HOME /usr/lib/jvm/
RUN export JAVA_HOME
# ENV PATH $JAVA_HOME/bin:$PATH
RUN mkdir -pv /root/.m2
# COPY resources/configure-maven /usr/local/bin/configure-maven
# RUN chmod a+x ./java --version
ENTRYPOINT ["java --version", "javac --version"]



