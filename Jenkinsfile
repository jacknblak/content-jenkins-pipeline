pipeline {
    agent any

    stages {
        stage ('build') {
            steps {
                sh 'echo Build Step Execution'
            }
        }
        stage ('run') {
            steps {
                sh 'echo Build Running Successfully'
                sh 'touch test.txt'
            }
        }
    }
    post {
        success {
            archiveArtifacts artifacts: 'test.txt', fingerprint: true
        }
    }
}
