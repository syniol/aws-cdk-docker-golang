# AWS CDK Docker
This could be used as a base for any new AWS CDK project. It uses Docker dind as a base image. It also 
includes the installation of following software programs:

 * AWS CLI
 * nodejs
 * npm
 * Go
 * Java
 * .NET 6
 * Python

It runs in a privileged mode due to use of docker inside the docker container. This allows CDK 
to build and publish docker images or synthesis Lambda's container runtime inside the running container.


## Useful Makefile Commands
There is a `makefile` at the root of this project, this would make running `docker-compose.yml` 
easier.

 * `make`: Builds docker images _(it ignores cached image & existing container)_
 * `make up`: Creates and runs docker container for `cdk`
 * `make down`: Stops & Removes `cdk` container
 * `make cdk`: Enters `cdk` container


## Useful CDK Commands
Start a new CDK project using Golang inside the `cdk` container using `make cdk` and then you 
could run all `cdk` commands; including the ones demonstrated below.

```bash
mkdir deploy
cd deploy
cdk init app --language go
```


### Links
* [Getting Started with AWS CDK V2](https://docs.aws.amazon.com/cdk/v2/guide/work-with-cdk-go.html)
* [API Reference](https://docs.aws.amazon.com/cdk/api/v2/docs/aws-construct-library.html)


#### Credits
 * [Hadi Tajallaei](mailto:hadi@syniol.com)

Copyright &copy; 2024, Syniol Limited. All rights reserved.
