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
      mali to: jedcanchola@gmail.com, subject: 'The Pipeline falied!!'
    }
  }
}