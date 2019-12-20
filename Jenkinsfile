node {
stage("checkout scm") {
    
    checkout scm
  
}    
stage("readiness check and connect to docker swarm) {
    dir('deploy/docker-swarm/') {
    sh "ls -lrt "       
}
}

stage("docker pull and build") {
    dir('deploy/docker-swarm/') {
    sh "docker-compose pull "
}
}
    
stage("docker push") {
    dir('deploy/docker-swarm/') {
   sh "docker-compose bundle"
    }
}
stage("deployment") {
    dir('deploy/docker-swarm/') {
    sh "docker deploy --bundle-file docker-swarm.dab sockshop"
    }
}
stage("check for frontend port ") {

    sh "docker service ls  | grep 3000*"
    
}
}


