// pipeline {
//     agent any

//     stages {
//         stage('Deploying Cloudformation Stack') {
//             steps {
//                 sh 'aws cloudformation deploy --template cloudformationstack.yml --stack-name Rameez-Stack'
//             }
//         }
//     }
// }
pipeline {
    agent any

    stages {
        stage('Hello') {
            steps {
                withCredentials([string(credentialsId: 'aws_access_key_id', variable: 'aws_access_key_id'), string(credentialsId: 'aws_secret_access_key', variable: 'aws_secret_access_key'), string(credentialsId: 'aws_region', variable: 'aws_region')]) {
                withEnv(['aws_region = $aws_region']) {
                    sh '''
                    echo $aws_region 
                    '''
                }
                
                
                // sh '''aws configure aws_access_key_id $aws_access_key_id
                //     aws configure aws_secret_key $aws_secret_access_key
                //     aws configure default.region $aws_region
                //     aws cloudformation deploy --template cloudformationstack.yml --stack-name Rameez-stack'''
                    }
            }
        }
    }
} 
