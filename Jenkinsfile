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

        stage('Test with env.variable') {
            environment {
                ENV_VAR_1 = 'environment variable 1'
                ENV_VAR_2 = 'environment variable 2'
            }
            steps {
                echo "${ENV_VAR_1}"
                echo "${ENV_VAR_2}"
            }
        }
    }
}
