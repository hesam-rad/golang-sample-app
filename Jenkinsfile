pipeline {
    agent any
    triggers {
        pollSCM('* * * * *')
    }
    stages {
        stage("Build") {
            steps {
                sh '''
                docker build . -t nexus.hesam.cf:5000/go-app-full:v1
                docker login nexus.hesam.cf:5000 -u $USER_DOCKER -p $PASS_DOCKER 
                docker push nexus.hesam.cf:5000/go-app-full:v1
                '''
            }
        }
        stage("Test") {
            steps {
               sh "docker images"
           }
        }
    }
}
