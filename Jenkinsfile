pipeline {
    agent any
    triggers {
        pollSCM('* * * * *')
    }
    stages {
        stage("Build") {
            steps {
                sh "docker images"
            }
        }
        stage("Test") {
            steps {
               sh "cat /tmp/jenkinstest.test"
           }
        }
    }
}
