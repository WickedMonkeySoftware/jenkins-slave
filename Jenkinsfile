node {
  stage 'checkout'
  checkout scm
  
  stage 'build'
  docker.withRegistry('http://10.0.0.4:5000') {
    def image = docker.build "withinboredom/jenkins-slave:${env.BRANCH_NAME}"
    
    stage 'push'
    image.push()
  }
}
