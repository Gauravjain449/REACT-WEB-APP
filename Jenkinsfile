pipeline {

    agent {

        docker {

            image 'node:alpine'

        }

    }

    environment {

        CI = 'true'
        
    }

        stages {

            stage('Install Dependencies') {

                steps {

                    sh 'npm install'
                }

            }
        }


}