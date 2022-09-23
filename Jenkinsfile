pipeline {
    agent any

    stages {
        stage('Unit tests') {
            steps {
                echo 'Unit tests...'
                dotnetTest project: 'TestWebApp.sln'
            }
        }
        stage('Build') {
            steps {
                echo 'Building...'
            }
        }
        stage('Deploy') {
            steps {
                echo 'Deploying....'
            }
        }
    }
}