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
                    steps {
                        sh './gradlew docker'
                    }
                }
                stage('Push Docker image') {
                    steps {
                        sh 'docker login --username=examplejenkins --password=qwerty12345'
                        sh './gradlew dockerPush'
                    }
                }
    }
}