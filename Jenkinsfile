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
                export aws_region=${AWS_REGION}
                export aws_access_key_id=${aws_access_key_id}
                export aws_secret_key=${aws_secret_key}
                echo $aws_region
                 '''              
                
                sh '''aws configure aws_access_key_id $aws_access_key_id
                    aws configure aws_secret_key $aws_secret_key
                    aws configure default.region $aws_region
                    aws cloudformation deploy --template cloudformationstack.yml --stack-name Rameez-stack'''
                }
        }
    }
} 
