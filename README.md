## setup

* install docker on host

* install jenkins on host

* `docker network create -d bridge staging`

* `docker run -d --hostname rabbitmq --name rabbitmq --network staging rabbitmq:latest`

* add a global shared library to jenkins 
  * `https://jenkins.io/doc/book/pipeline/shared-libraries/#global-shared-libraries`
  * point to `https://github.com/uni-10yg/deployment-pipeline`

* point jenkins to repositories
