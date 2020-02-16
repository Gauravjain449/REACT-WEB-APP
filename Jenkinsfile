pipeline {

    agent {
        docker {
            image 'node:alpine'
        }
    }

    environment {
        CI = 'true'
    }

    options {
        timeout(time: 1, unit: 'HOURS')
    }

    stages {
        
        stage('Install Dependencies') {
            steps {
                    sh 'npm install'
                }
            }
        }


}