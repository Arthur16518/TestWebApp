pipeline {
    agent any

    stages {
        stage('Unit tests') {
            steps {
                withDotNet {             
                    sh("ls");
                    dotnetTest();
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