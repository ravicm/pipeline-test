pipeline {
  agent any
  stages {
    stage('SCM') {
      steps {
        echo 'This is stage 1'
      }
    }
    stage('Build') {
      steps {
        echo 'Building artifact'
      }
    }
    stage('Test') {
      steps {
        echo 'Testing artifact'
      }
    }
    stage('User Input') {
      steps {
        input 'Do you want to deploy?'
        echo 'This is User input stage step2'
      }
    }
    stage('Deploy') {
      steps {
        sh 'echo "Deploying to dev env"'
      }
    }
  }
}