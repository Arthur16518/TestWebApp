pipeline {
    agent any

    stages {
        stage('Unit tests') {
            steps {
                echo 'Unit tests...'
                withDotNet() {   
                    sh 'dotnet test TestWebApp.sln -v q'
                }
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