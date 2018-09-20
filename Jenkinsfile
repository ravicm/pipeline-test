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
      }
      steps {
                script {
                    env.RELEASE_SCOPE = input message: 'Do you want to deploy?', ok: 'Release!',
                            parameters: [choice(name: 'RELEASE_SCOPE', choices: 'patch\nminor\nmajor', description: 'What is the release scope?')]
                }
                echo "${env.RELEASE_SCOPE}"
     }
    }
    stage('Deploy') {
      steps {
        sh 'echo "Deploying to dev env"'
      }
    }
  }
}
