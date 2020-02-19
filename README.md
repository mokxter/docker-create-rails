# Docker Create Rails 

This is just a Dockerfile for to use for creating a docker image for creating a new Rails app.

## Usage

### Building the image
```
docker build -t docker-create-rails --build-arg USER_ID=$(id -u) --build-arg GROUP_ID=$(id -g) -f Dockerfile.rails .
```

### Creating a new rails app
```
docker run -it -v $PWD:/opt/app docker-create-rails rails new --skip-bundle RAILS_APP_NAME
```
