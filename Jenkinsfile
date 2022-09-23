pipeline {
    agent any

    stages {
        stage('Unit tests') {
            steps {
                withDotNet() {   
                    sh(returnStdout: true, script: "dotnet --list-sdks")
                    sh(returnStdout: true, script: "dotnet test TestWebApp.sln -v q")
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