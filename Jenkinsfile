pipeline {
    agent any

    stages {
        stage('Unit tests') {
            steps {
                bat('dotnet test');
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