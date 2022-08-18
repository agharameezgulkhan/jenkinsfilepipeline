pipeline {
    agent {label 'slave2'}
    stages {
        stage('Deploying on slave2') {
            steps {
                sh 'mv build/* /var/www/html'
            }
        }
    }
}
