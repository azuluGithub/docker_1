FROM ruby:2.5

RUN bash -l -c "gem install rails"

RUN apt-get update
RUN apt-get -y install node.js
RUN apt-get -y install yarn 

RUN apt-get install sqlite3 -y
RUN rails new app

ADD https://raw.githubusercontent.com/rails/webpacker/master/lib/install/config/webpacker.yml app/config/

RUN bash -l -c "cp -r app opt/"
RUN bash -l -c "rm -rf app"

WORKDIR opt/app
EXPOSE 3000

RUN bundle install
RUN rake db:migrate
RUN rake db:seed

#-------------------------- REF ----------------------
#https://hub.docker.com/_/rails/
#-----------------------------------------------------
