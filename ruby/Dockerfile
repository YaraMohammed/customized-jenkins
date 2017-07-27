FROM yaramohamed/jenkins-ubuntu16:vGradle
USER root
RUN apt-add-repository ppa:brightbox/ruby-ng
RUN apt-get update
RUN apt-get install ruby2.4 ruby2.4-dev -y
RUN gem install bundler
RUN gem install fastlane -NV
