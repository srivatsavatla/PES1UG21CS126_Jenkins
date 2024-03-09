pipeline{
  agent any 
  stages {
    stage('Build') {
      steps {
        sh 'g++ hello.cpp -o output'
        build 'PES1UG21CS126-1'
      }
    }
    stage('Test') {
      steps {
        sh './output'
      }
    }
    stage('Deploy') {
      steps {
        echo 'Deploy'
      }
    }
  }
    post {
      failure {
        error 'Pipeline failed'
      }
    }
}
