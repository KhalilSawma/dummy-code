pipeline {
  agent { dockerfile true }
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
}
