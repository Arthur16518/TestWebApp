pipeline {
    agent any

    stages {
        stage('Unit tests') {
            steps {
                echo 'Unit tests...'
                withDotNet {   
                    dotnetTest project: 'TestWebApp.sln'
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