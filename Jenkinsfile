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
        timeout (time:5, unit: 'DAYS'){
          input 'Does staging looks look ?'
        }
      }
    }

  }
  post{
    always {
      deleteDir()
    }
  }

}
