# Minimal-and-secure-Docker-images
I've created a simple framework for creating minimal and secure Docker images based on Alpine. It consist of a Dockerfile-template, a number of standardized constants, a few helper-images, and structured shell scripts.

## The Dockerfile-template
The Dockerfile-template is divided into six blocks, of which three are mandatory, and two are static: 
* TAG-block <- mandatory!
* ARG-block
* Static-block-1 <- mandatory!
* ENV-block
* Static-block-2 <- mandatory!
* End-block

### The TAG-block
This block contains only the TAG-constant, defined in an ARG statement. If the content-, base- or helper-images, used during the build process, are based on different Alpine builds, then there is a risc of mismatching system libraries. The TAG-constant makes sure all stage images are based on the same Alpine base image.

### The ARG-block
This block contains ARG statements, setting any of the following constants:
