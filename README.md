## setup

* install docker on host

* install jenkins on host

* run `docker network create -d bridge staging`

* run `docker run -d --hostname rabbitmq --name rabbitmq --network staging rabbitmq:latest`

* add a global shared library to jenkins 
  * `https://jenkins.io/doc/book/pipeline/shared-libraries/#global-shared-libraries`
  * point to `https://github.com/uni-10yg/deployment-pipeline`
  * tick `Load implicitly` and set `Default version` to `master`

* point jenkins to repositories

* run builds

* send HTTP POST requests to `localhost:8081`
  * request body `{ "phrase": "your text" }`
  * request header `Content-Type: application/json`

* tail log of service-a with `docker logs -f service-a` to see incoming messages get stored in DB
