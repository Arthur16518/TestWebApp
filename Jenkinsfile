pipeline {
    agent any
    stages {
        stage('Unit tests') {
            steps {
            sh("${tool 'dotnet6'}/dotnet test TestWebApp.sln")
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