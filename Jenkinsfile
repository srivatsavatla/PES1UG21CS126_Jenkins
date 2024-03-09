pipeline {
    agent any
    stages {
        stage('Build') {
            steps {
                sh 'set -e; g++ -o output hello.cpp || { echo "Compilation failed"; exit 1; }'
            }
        }
        stage('Test') {
            steps {
                sh './output'
            }
            post {
                success {
                    junit 'reports/**/*.xml'
                }
            }
        }
        stage('Deploy') {
            steps {
                echo 'Deploy'
            }
            when {
                branch 'main'
            }
        }
    }
    post {
        always {
            cleanWs()
        }
    }
}
