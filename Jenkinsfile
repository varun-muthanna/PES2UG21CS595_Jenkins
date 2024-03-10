pipeline {
  agent any
  stages {
    stage('Build') {
      steps {
        sh 'g++ -o task5 main/hello.cpp'
        echo 'Build Successful!'
      }
    }
    stage('Test') {
      steps {
        sh './task5'
        echo 'Test Successful!'
      }
    }
    stage('Deploy') {
      steps {
        sh 'nonexistent_command' // Intentional Error
        echo 'Successfully deployed!'
      }
    }
  }
  post {
    failure {
      echo 'Pipeline Failed!'
    }
  }
}
