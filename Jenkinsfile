pipeline {
    agent any
    stages {
        stage('Unit tests') {
            environment {
                DOTNET_SYSTEM_GLOBALIZATION_INVARIANT = 1
            }
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