pipeline {
    agent none

    stages {
        stage('Deploying on slave2') {
            agent {label: slave2}
            steps {
                sh 'mv index.html /var/www/html'
            }
        }
    }
}
