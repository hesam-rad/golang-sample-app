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
                docker login nexus.hesam.cf:5000  -uAdmin -p Aa@123456
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

