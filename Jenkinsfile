node {
stage("checkout scm") {
    
    checkout scm
  
}    
stage("changing dir to docker swarm") {
    dir('microservices-demo/deploy/docker-swarm/') {
    ls -lrt 
        
}
}

stage("docker pull and build") {
    sh "echo 'this is the docker pull stage'"
}
stage("docker push") {
    
   sh "echo 'this is the docker push stage'"
    }
   
stage("deployment") {
    sh "echo 'this is the deployment stage'"
    }
}


