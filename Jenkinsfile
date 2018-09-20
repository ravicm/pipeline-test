pipeline {
  agent any
  stages {
    stage('Stage 1') {
      steps {
        echo 'This is stage 2'
      }
    }
    stage('Stage 2') {
      steps {
        input 'Do you want to deploy?'
      }
    }
  }
}