pipeline {
    agent {
        // Define agent details here
    }
    environment {
        AWS_ACCESS_KEY_ID     = credentials('jenkins-aws-secret-key-id')
        AWS_SECRET_ACCESS_KEY = credentials('jenkins-aws-secret-access-key')
    }
    stages {
        stage('Example stage 1') {
            steps {
                echo "ID: ${AWS_ACCESS_KEY_ID}"
            }
        }
        stage('Example stage 2') {
            steps {
                echo "Secret: ${AWS_SECRET_ACCESS_KEY }"
            }
        }
    }
}