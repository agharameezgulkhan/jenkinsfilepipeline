pipeline {
    agent {label 'slave2'}
    stages {
        stage('Deploying on slave2') {
            steps {
                sh 'sudo mv build/* /var/www/html'
            }
        }
    }
}
