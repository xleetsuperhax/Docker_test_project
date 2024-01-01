This is a small project aimed at demonstrating basic functionalities of docker in the form of images and pulling/running docker images.

I will assume that you have downloaded docker and have managed to log in the docker service through the terminal.

To run this project, run the following 2 commands in the terminal.

docker pull xleetsuperhax/quote_generator:latest
docker run -p 8080:8080 xleetsuperhax/quote_generator

If you want to run this image in the docker desktop application, it is required to set the port to 8080 in the optional settings upon pressing the run key.

As for the application itself, it is a simple vue-based single-page-application that pulls a random quote from the api when a button is clicked.
