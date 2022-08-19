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
                sh '''echo $aws_access_key_id
                    echo $aws_secret_access_key
                    echo $aws_region'''
                    }
            }
        }
    }
} 
