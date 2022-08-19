pipeline {
    agent any

    stages {
        stage('Deploying Cloudformation Stack') {
            steps {
                sh 'aws cloudformation deploy --template cloudformationstack.yml --stack-name Rameez-Stack'
            }
        }
    }
}