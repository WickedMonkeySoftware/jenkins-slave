node {
  stage 'build'
  docker.withRegistry('http://10.0.0.4') {
    def image = docker.build "withinboredom/jenkins-slave:${env.BRANCH_NAME}"
    
    stage 'push'
    image.push()
  }
}
