pipeline {
  agent any
  stages {
    stage('Build'){
      step{
        sh 'ls'
      }
    }

  stage('Deploy - Staging')
    echo 'Deploying to staging'
    sh 'ls'
  }

  post{
    always {
      deleteDir()
    }
  }
}
