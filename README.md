## sample microservice demo for internal use only - improvised by Rajib Mitra

## for docker swarm mode deployment follow these steps 

1. cd microservices-demo/deploy/docker-swarm/
2. docker swarm init
3. docker-compose pull
4. docker-compose bundle
5. docker deploy --bundle-file docker-swarm.dab sockshop
