pipeline {
  agent any
  stages {

    stage('Build'){
      steps {
        sh 'ls'
      }
    }

    stage('Deploy - Staging') {
      steps {
        echo 'Deploying to staging'
        sh 'ls'
        // sh './deploy staging'
        timeout (time:5, unit: 'DAYS'){
          input 'Does staging looks look ?'
        }
      }
    }

    stage('Deploy - Production'){
      steps{
        echo 'Deploying to production'
        sh 'ls'
        // sh './deploy production'
      }
    }

  }
  post{
    always {
      deleteDir()
    }
  }

}
