pipeline {
  agent { dockerfile true }
  stages {
    stage('Test') {
      steps {
        sh '''
          curl localhost:80
        '''
      }
    }
  }
}
