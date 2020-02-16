pipeline {

    // agent {
    //     docker {
    //         image 'node:alpine'
    //     }
    // }

    agent any

    environment {
        PASSWORD = credentials('DOCKER_PASSWORD')
        REPOSITORY_TAG="${DOCKER_HUB_USER_NAME}/client-app:${BUILD_ID}"
        CI = 'true'
    }

    options {
        timeout(time: 1, unit: 'HOURS')
    }

    stages {

        stage('Clean WS') {
            steps {
                cleanWs()
                git credentialsId: 'GitHub', url: "https://github.com/Gauravjain449/REACT-WEB-APP.git"
            }

        }
        
        stage('Docker build image') {
            steps {
                     sh 'docker build -t ${REPOSITORY_TAG} -f Dockerfile.dev .'
                }
            }
        }


}