# server-boilerplate

## Tech Stack
Docker is used to keep the provisioning of environments rapid, most of the work is done in tutums [apache-php](https://hub.docker.com/r/tutum/apache-php/). The base image can easily be swapped out for a different, language specific option.

##### Setting up docker

To get started you will need to prepare your system to work with docker, see [Getting started with docker](https://docs.docker.com/mac/).

The docker image is located in a private repo [here](https://hub.docker.com/r/specimin/boilerplate/).

Once you are setup you can run the following steps to get the docker container running.

Build the image

    docker build -t specimin/boilerplate .


Bind the necessary ports

    docker run -d -p 80:80 specimin/boilerplate

Get the docker IP

    docker-machine ip default

Now test the connection to the machine

    curl http://<dockerIP>:<port>

Get a shell into the docker container

    sudo docker exec -i -t <containerId>

![docker](https://docs.docker.com/dist/assets/images/logo.png)
![composer](https://getcomposer.org/img/logo-composer-transparent5.png)
![silex](https://bolt.cm/thumbs/606x400r/2014-12/featureimg_silexsymfony.png)
