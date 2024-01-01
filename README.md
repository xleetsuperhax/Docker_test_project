This is a small project aimed at demonstrating basic functionalities of docker in the form of images and pulling/running docker images.

To run this project, run the following 2 commands in the commandline

docker pull xleetsuperhax/quote_generator:latest
docker run -p 8080:8080 xleetsuperhax/quote_generator

If you want to run this image in the docker desktop application, it is required to set the port to 8080 in the optional settings upon pressing the run key.

As for the application itself, it is a simple vue-based single-page-application that pulls a random quote from the api when a button is clicked.

If you want to pull and run the vue application directly from github, you can run the project with the following commands after cloning it to your local machine.

# quote-generator

## Project setup
```
npm install
```

### Compiles and hot-reloads for development
```
npm run serve
```

### Compiles and minifies for production
```
npm run build
```

### Lints and fixes files
```
npm run lint
```

### Customize configuration
See [Configuration Reference](https://cli.vuejs.org/config/).
