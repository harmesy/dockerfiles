FROM ubuntu:latest
MAINTAINER Matt Harmes "matt@harmes.ca"

RUN rm /bin/sh && ln -s /bin/bash /bin/sh
RUN echo 'gem: --no-document' > ~/.gemrc
RUN apt-get -y update
RUN apt-get -y install git curl build-essential nodejs
RUN gpg --keyserver hkp://keys.gnupg.net --recv-keys 409B6B1796C275462A1703113804BB82D39DC0E3
RUN \curl -sSL https://get.rvm.io | bash -s stable --ruby
RUN echo "source /usr/local/rvm/scripts/rvm" >> ~/.bashrc
CMD ["/bin/bash"]
