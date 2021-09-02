pipeline {
    agent any
    stages {
        stage("Build") {
            steps {
                sh "touch /tmp/jenkinstest.test"
                sh "echo "Stage test > /tmp/jenkinstest.test"
            }
        }
    }
}
