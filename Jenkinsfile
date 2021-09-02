pipeline {
    agent any
    triggers {
        pollSCM('* * * * *')
    }
    stages {
        stage("Build") {
            steps {
                sh "touch /tmp/jenkinstest.test"
                sh "echo test2 > /tmp/jenkinstest.test"
            }
        }
    }
}
