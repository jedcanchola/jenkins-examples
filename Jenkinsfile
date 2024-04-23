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
      mail bcc: '', body: 'Sorry it  failed', cc: '', from: '', replyTo: '', subject: 'Pipeline Failed', to: 'jedcanchola@gmail.com'
    }
  }
}