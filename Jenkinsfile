node {
stage("checkout scm") {
    
    checkout scm
  
}    
stage("changing dir to docker swarm") {
    dir('deploy/docker-swarm/') {
    sh "ls -lrt "       
}
}

stage("docker pull and build") {
    sh "docker-compose pull "
}
stage("docker push") {
    
   sh "docker-compose bundle"
    }
   
stage("deployment") {
    sh "docker deploy --bundle-file docker-swarm.dab sockshop"
    }
}


