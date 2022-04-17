# make an aws batch job to run on ec2

## Steps
- make an ec2 with docker
- check compute env has stack listed
- check job definition
- check queues
- run job and check CW logs

```
docker pull <image name>
docker run -it image /bin/bash
docker history
docker ps -a
docker container ls

```