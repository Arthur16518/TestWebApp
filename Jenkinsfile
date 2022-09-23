pipeline {
    agent any

    stages {
        stage('Unit tests') {
            steps {
                echo 'Unit tests...'
                sh 'find ~/ -name dotnet'
                sh "dotnet test TestWebApp.sln -v q"
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