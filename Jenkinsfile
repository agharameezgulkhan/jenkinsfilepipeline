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

    environment{
        aws_access_key_id = credentials('aws_access_key_id')
        aws_secret_key = credentials('aws_secret_access_key')
        aws_region = credentials('aws_region')
    }

    stages {
        stage('Hello') {
            steps {
                sh '''
                export AWS_REGION=${aws_region}
                export AWS_ACCESS_KEY_ID=${aws_access_key_id}
                export AWS_SECRET_ACCESS_KEY=${aws_secret_key}
                 '''              
                
                sh '''aws cloudformation deploy --template cloudformationstack.yml --stack-name Rameez-stack'''
                }
        }
    }
} 
