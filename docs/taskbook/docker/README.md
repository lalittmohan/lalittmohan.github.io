> Docker is an open plateform for developers and sysadmins to build, ship, and run distributed applications.consisting of docker engine, a portable lightweight runtime and packaging tools and docke hub, a cloud service for sharing applications and automation workflows

docker enable apps to be quickly assembled from components and eliminated the friction between development , QA and production environments.

containers: [images here]

Reduce efforts to build and maintain consistent development environments

issue:
- handbook for environment setup with different os,configuration,version needs to be maintained
- Needs install & configure several tools like Git ,JDK,NPM ,Composer etc
- Different developer machine tools are not equally on each machine (window,linux,mac) & different behaviour
- Developer are not continously updating their environment when updated handbook
- Cost lot of time to setup & configure for development environment

solutions 1:
pros:
- Virtual machines like oracleVM, Vagrant resolve all above problem but require high memory
  crons:
- Large VM size
- Everybody Needs same virtualization software
- High memory usage
- Installation & configuration needs to be created

solutions 2:
pro:
- Docker container with necessary tools and configurations defined in Dockerfile which can be managed withing VCS (github|gitlab|bitbucket)
- Container can be run on all different kinds of developer machines
- running same container behind co-operate proxy with username/password and inhome office without proxy
- it solve user accessible issue in linux due to user rights
- on Mac shared volumns are working very slow within docker machine due to issue with vobxsf


application may be shipped as container
- deliverable & development shared same base container || same container in production|staging|development
- build server is also a docker container itself

DOCKER vs vagrant

- no data overhead compared to vagrant
- no rsync or nfs-mount needed for development environment (union file system)
- extreme fast devleopment & environment setup
- same behaviour everywhere
- No server provisioning
- roll out testing server updates withing seconds to all clients
- ablity to cluster containers across multiple servers
- test very complex server setup locally



Development environment (VCS client,IDE,buid tools ) & configuration to develop build,test
developer machine is computer with an arbirary opration system which is used by developer to develop ,buid and a test a software project.
