pipeline {
  agent any
  
  stages {
    stage('No op'){
      steps {
        sh 'ls'
      }
    }
  }

  post {
    always {
      echo 'One way or another, we gonna delete our workspace'
      deleteDir()
    }

    success {
      echo 'You rock!'
    }

    unstable {
      echo 'Build is unstable'
    }

    failure {
      echo 'Oh man..'
    }

    changed {
      echo 'Things were different before'
    }

  }
}
