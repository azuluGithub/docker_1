FROM ruby

RUN apt-get update  && apt-get install -y build-essential libpq-dev nodejs sqlite3

ONBUILD COPY app /opt/app
ONBUILD WORKDIR /opt/app

ONBUILD EXPOSE 3000
ONBUILD RUN bundle install
ONBUILD RUN rake db:migrate
ONBUILD RUN rake db:seed

#-------------------------- REF ----------------------
#https://hub.docker.com/_/rails/
#https://takacsmark.com/dockerfile-tutorial-by-example-dockerfile-best-practices-2018/#1-create-the-dockerfile
#docker build -t ft-rails:on-build .i
#ONBUILD => instructions that will be executed when your image is used as the base image of another Dockerfile
#EXPOSE => An important instruction to inform your users about the ports your application is listening on
#-----------------------------------------------------
