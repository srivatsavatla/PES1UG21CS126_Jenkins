pipeline {
    agent any
    stages {
        stage('Build') {
            steps {
                dir('main') {
                    sh 'g++ hello.cpp -o output'
                }
            }
        }
        stage('Test') {
            steps {
                dir('main') {
                    sh './output'
                }
            }
        }
        stage('Deploy') {
            steps {
                echo 'deploy'
            }
        }
    }
    post {
        failure {
            error 'Pipeline failed'
        }
    }
}
