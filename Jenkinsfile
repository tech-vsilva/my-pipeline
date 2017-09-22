pipeline {
    agent any

    environment {
        DISABLE_AUTH = 'true'
        DB_ENGINE    = 'sqlite'
    }

    stages {
        stage('Build') {
            steps {
                sh 'printenv'
                echo "${DISABLE_AUTH}"
                echo "${DB_ENGINE}"
            }
        }
    }
}
