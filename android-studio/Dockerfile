FROM yaramohamed/jenkins-ubuntu16:vRuby
USER root
RUN wget https://dl.google.com/dl/android/studio/ide-zips/2.3.3.0/android-studio-ide-162.4069837-linux.zip
RUN unzip android-studio-ide-162.4069837-linux.zip -d /opt
RUN echo echo PATH=/opt/android-studio/bin:$PATH >> ~/.bashrc
