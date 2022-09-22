pipeline {
    agent any

    stages {
        stage('Unit tests') {
            steps {
                sh('dotnet test');
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