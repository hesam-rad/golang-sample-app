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
                echo $PASS_DOCKER | docker login nexus.hesam.cf:5000  -u$DOCKER_USER --password-stdin
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

