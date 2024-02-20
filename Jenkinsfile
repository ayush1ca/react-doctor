// in root group sudo chown permission in /var/www/html with 777 and jenkins also add www-data in root 

// pipeline {
//     agent {
//         any {
//             // i mage 'node:6-alpine'
//             args '-p 3000:3000'
//         }
//     }
//     // agent 
//     tools {nodejs "node"}
//     environment {
//             CI = 'true'
//         }
//     stages {
//         stage('Build') {
//             steps {
//                 sh 'node -v'
//                 sh 'npm install'
//             }
//         }
//         // stage('Test') {
//         //     steps {
//         //         sh 'npm test'
//         //     }
//         // }
//         stage('Deliver') {
//             steps {
//                 // sh 'npm install -g serve'
//                 // sh 'npm install react-scripts'
//                 sh 'pwd'
//                 sh 'npm run build --max-old-space-size=1024'
//                 sh 'cp -r * /var/www/html'
//                 echo 'Visit http://localhost:3000 to see your Node.js/React application in action.'
//                 // sh 'npm start'
//                 // input message: 'Finished using the web site? (Click "Proceed" to continue)'
//                 echo 'copy all filessss'
                
//             }
//         }   
     

//     }
// }


pipeline {
    agent {
        any {
            // i mage 'node:6-alpine'
            args '-p 3000:3000'
        }
    }
    // agent 
    tools {nodejs "node"}
    environment {
            CI = 'true'
        }
    stages {
        stage('Build') {
            steps {
                sh 'node -v'
                sh 'npm install'
            }
        }
        // stage('Test') {
        //     steps {
        //         sh 'npm test'
        //     }
        // }
        stage('Deliver') {
            steps {
                // sh 'npm install -g serve'
                // sh 'npm install react-scripts'
                sh 'npm run build --max-old-space-size=1024'
                sh 'sudo scp -i /home/ubuntu/ec2-testing.pem -r * ubuntu@3.89.49.116:/var/www/html'
                echo 'Visit http://localhost:3000 to see your Node.js/React application in action.'
                // sh 'npm start'
                // input message: 'Finished using the web site? (Click "Proceed" to continue)'
                echo 'copy all filessss'
                
            }
        }   
     

    }
}