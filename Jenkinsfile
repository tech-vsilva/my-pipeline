pipeline {
    agent any
    stages {
        stage('Build') {
            steps {
                sh 'touch file_aa.txt'
                sh 'touch file_ab.txt'
                sh 'touch file_ba.txt'
                sh 'touch file_bb.txt'
            }
        }
    }
}
