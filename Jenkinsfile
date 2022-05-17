pipeline {
    agent any

    triggers {
        pollSCM '* * * * *'
    }
    stages {
        stage('Build') {
            steps {
                   echo 'Build'
            }
        }
        stage('Test') {
            steps {
                   echo 'Test'
            }
        }
        stage('Build Docker image') {
            environment {
                GRADLE_OPTS = '-Djsse.enableSNIExtension=false'
            }
            steps {
                sh './gradlew docker'
            }
        }

    }
}