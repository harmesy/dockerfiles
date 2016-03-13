FROM harmesy/ruby:latest
MAINTAINER Matt Harmes "matt@harmes.ca"

ENV DEBIAN_FRONTEND "noninteractive"
RUN echo "deb http://apt.postgresql.org/pub/repos/apt/ trusty-pgdg main" > /etc/apt/sources.list.d/pgdg.list
RUN apt-get install -y wget
RUN wget --quiet -O - https://www.postgresql.org/media/keys/ACCC4CF8.asc | apt-key add -
RUN apt-get update
RUN apt-get install -y libpq-dev postgresql-client-9.4
RUN /bin/bash -c "source /usr/local/rvm/scripts/rvm; gem install rails --no-document"
EXPOSE 3000
CMD ["/bin/bash"]
