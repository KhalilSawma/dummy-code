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
    stage('Build') {
    steps {
        sh 'docker build -t khalilsawma/jenkins-docker-hub .'
      }
    }
    stage('Login') {
      steps {
        sh 'echo $DOCKERHUB_CREDENTIALS_PSW | docker login -u $DOCKERHUB_CREDENTIALS_USR --password-stdin'
      }
    }
    stage('Push') {
      steps {
        sh 'docker push khalilsawma/jenkins-docker-hub'
      }
    }
  }
  post {
    always {
      sh 'docker logout'
    }
  }
  }
}
