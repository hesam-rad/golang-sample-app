pipeline {
    agent any
    triggers {
        pollSCM('* * * * *')
    }
    stages {
        stage("Build") {
            steps {
                sh "touch /tmp/jenkinstest.test"
                sh "echo test > /tmp/jenkinstest.test"
            }
        }
    }
}
