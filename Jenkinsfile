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
    }
}