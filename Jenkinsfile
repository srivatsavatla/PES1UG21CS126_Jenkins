pipeline {
    agent any

    stages {
        stage('Build') {
            steps {
                // Compile the .cpp file using shell script
                sh 'g++ -o PES1UG21CS126-1 hello.cpp'
            }
        }
        stage('Test') {
            steps {
                // Print output of .cpp file using shell script
                sh './PES1UG21CS126-1'
            }
        }
        stage('Deploy') {
            steps {
                // Add deployment steps if needed
                echo 'Deployment skipped for this demo'
            }
        }
    }

    post {
        failure {
            echo 'Pipeline failed'
        }
    }
}
