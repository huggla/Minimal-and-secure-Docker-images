# Minimal-and-secure-Docker-images
I've created a simple framework for creating minimal and secure Docker images based on Alpine. It consist of a Dockerfile-template, a number of standardized constants, and a few helper-images.

## The Dockerfile-template
The Dockerfile-template is divided into six blocks, of which three is mandatory: 
* TAG-block <- mandatory!
* ARG-block
* Static-block-1 <- mandatory!
* ENV-block
* Static-block-2 <- mandatory!
* End-block
