FROM yaramohamed/jenkins-ubuntu16:1.0.0
USER root
RUN wget https://dl.google.com/android/archives/android-sdk-linux_x86-1.6_r1.tgz
RUN tar xvzf android-sdk*.tgz -C /tmp/
RUN apt-get update
RUN apt-get install lib32z1 lib32ncurses5 lib32stdc++6 -y
RUN chmod -R +xr /tmp/android-sdk-linux*
RUN mv /tmp/android-sdk-linux* /opt/android-sdk-linux
USER jenkins
RUN echo export PATH=/opt/android-sdk-linux/tools:/opt/android-sdk-linux/platform-tools:$PATH >> ~/.bashrc
