FROM yaramohamed/jenkins-ubuntu16:1.0.0
USER root
RUN wget https://dl.google.com/android/archives/android-sdk-linux_x86-1.6_r1.tgz
RUN tar xvzf android-sdk*.tgz -C /tmp/
RUN apt-get update
RUN apt-get install lib32z1 lib32ncurses5 lib32stdc++6 -y
RUN chmod -R +xr /tmp/android-sdk-linux*
RUN mv /tmp/android-sdk-linux* /opt/android-sdk-linux
FROM yaramohamed/jenkins-ubuntu16:vSDK
USER root
RUN wget https://services.gradle.org/distributions/gradle-3.3-bin.zip
RUN mkdir /opt/gradle
RUN unzip -d /opt/gradle gradle-3.3-bin.zip
RUN apt-add-repository ppa:brightbox/ruby-ng
RUN apt-get update
RUN apt-get install ruby2.4 ruby2.4-dev -y
RUN gem install bundler
RUN gem install fastlane -NV
RUN wget https://dl.google.com/dl/android/studio/ide-zips/2.3.3.0/android-studio-ide-162.4069837-linux.zip
RUN unzip android-studio-ide-162.4069837-linux.zip -d /opt
RUN echo export PATH=/opt/android-sdk-linux/tools:/opt/android-sdk-linux/platform-tools:/opt/gradle/gradle-3.3/bin:/opt/android-studio/bin:$PATH >> ~/.bashrc
