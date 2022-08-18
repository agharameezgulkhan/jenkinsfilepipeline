pipeline {
    agent {label 'slave2'}
    stages {
        stage('Deploying on slave2') {
            steps {
                sh 'cd /var/www/html'
                sh 'rm -d -r -y *'
            }
        }
    }
}
