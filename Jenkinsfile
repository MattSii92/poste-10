 pipeline {
    agent any
    environment {
        DOCKER_USER = ''
    }
 
    stages {
 
        stage('Login Docker') {
            steps {
                withCredentials([string(credentialsId: 'poste00-DOCKER_PASSWORD', variable: 'DOCKER_PASS')]) {
                    sh '''
                        echo "$DOCKER_PASS" | docker login -u "$DOCKER_USER" --password-stdin
                    '''
                }
            }
        }
 
    }
}