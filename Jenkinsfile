pipeline {
    agent {
        node {
            label 'docker-local-compose-v1'
        }
    }
    stages {
        stage ('Checkout SCM') {
            steps {
                checkout scm
            }
        }
    }
}