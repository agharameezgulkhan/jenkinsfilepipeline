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
        AWS_REGION = credentials('aws_access_key_id')
    }

    stages {
        stage('Hello') {
            steps {
                sh '''
                echo $AWS_REGION
                 '''              
                
                // sh '''aws configure aws_access_key_id $aws_access_key_id
                //     aws configure aws_secret_key $aws_secret_access_key
                //     aws configure default.region $aws_region
                //     aws cloudformation deploy --template cloudformationstack.yml --stack-name Rameez-stack'''
                }
        }
    }
} 
