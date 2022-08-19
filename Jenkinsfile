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
                echo $AWS_ACCESS_KEY_ID
                echo $AWS_SECRET_ACCESS_KEY
                echo $AWS_REGION
            }
        }
    }
} 
