pipeline {
    agent any

    stages {
        stage('Build') {
            steps {
                // Remove any previously compiled artifacts
                sh 'rm -f PES1UG21CS126-1'

                // Compile the .cpp file using g++
                sh 'g++ -o PES1UG21CS126-1 hello.cpp'
            }
        }

        stage('Test') {
            steps {
                // Print output of .cpp file using shell script
                sh "./PES1UG21CS126-1"
            }
        }

        stage('Deploy') {
            steps {
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
