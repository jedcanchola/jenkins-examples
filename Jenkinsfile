pipeline {
  agent any

  stages {
    stage ('Test') {
      steps {
        sh 'make check'
      }
    }
  }
  post {
    always {
      junit '**/target/*.xml'
    }
    failure {
      slackSend channel: 'alerts', message: 'Pipeline failed'
    }
  }
}