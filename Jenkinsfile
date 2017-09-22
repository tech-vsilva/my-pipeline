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
      currentBuild.*
      // mail to:'valter.silva@orderbird.com', subject:'Build were successful', body: 'Your build were successful'
    }

    unstable {
      echo 'Build is unstable'
    }

    failure {
      echo 'Oh man..'
      // mail to:'valter.silva@orderbird.com', subject:'Build has failed (test)', body: 'Your build has failed'
    }

    changed {
      echo 'Things were different before'
    }

  }
}
