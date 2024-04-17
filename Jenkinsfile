pipeline {
    agent any

    environment {
        USER_CREDS     = credentials('USER_CREDS')
        USER_CREDS_USR  = credentials('USER_CREDS')
        USER_CREDS_PSW  = credentials('USER_CREDS')
    }

    stages {
        stage('Example stage 1') {
            steps {
                echo "User credentials: ${USER_CREDS}"
            }
        }
        stage('Example stage 2') {
            steps {
                echo "Username: ${USER_CREDS_USR}"
                echo "Password: ${USER_CREDS_PSW}"
            }
        }
    }
}