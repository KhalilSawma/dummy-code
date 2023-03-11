pipeline {
  agent { dockerfile true }
  stages {
    stage('Test') {
      steps {
        sh '''
          curl 54.175.133.199:80
        '''
      }
    }
  }
}
