pipeline {
  agent any
  stages {
    stage('Build'){
      steps {
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
