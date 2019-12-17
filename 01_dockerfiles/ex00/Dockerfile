FROM alpine

RUN apk update && \
	apk upgrade && \
	apk add vim

ENTRYPOINT vim

#------------------------------------- NOTES --------------------------------------------
#A Dockerfile is a text file that defines a Docker image
#a Dockerfile is a step by step definition of building up a Docker image
#You use ENTRYPOINT as the main executable of your image
#----------------------------------------------------------------------------------------


#------------------------------------- REF ----------------------------------------------
#https://takacsmark.com/dockerfile-tutorial-by-example-dockerfile-best-practices-2018/#1-create-the-dockerfile

#docker build -t ex00 .
#docker run --rm -ti ex00 /bin/sh
#vim --v
#----------------------------------------------------------------------------------------
