FROM yaramohamed/jenkins-ubuntu16:vSDK
USER root
RUN wget https://services.gradle.org/distributions/gradle-3.3-bin.zip
RUN mkdir /opt/gradle
RUN unzip -d /opt/gradle gradle-3.3-bin.zip
USER jenkins
RUN echo export PATH=$PATH:/opt/gradle/gradle-3.3/bin >> ~/.bashrc
