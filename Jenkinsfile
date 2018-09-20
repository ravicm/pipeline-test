pipeline {
  agent any
  stages {
    stage('Stage 2') {
      parallel {
        stage('Stage 2') {
          steps {
            echo 'This is after user input'
          }
        }
        stage('Stage 1') {
          steps {
            echo 'This is stage 1'
          }
        }
      }
    }
  }
}