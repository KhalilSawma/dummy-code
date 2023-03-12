pipeline {
  agent { dockerfile true }
  environment {
    DOCKERHUB_CREDENTIALS = credentials('dockerhub')
  }
  stages {
    stage('Test') {
      steps {
        sh '''
          nginx -v
          curl 54.175.133.199
        '''
      }
    }
}
