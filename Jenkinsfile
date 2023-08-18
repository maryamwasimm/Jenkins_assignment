pipeline{
    agent any
    stages{
        stage('Checkout'){
            steps{
                checkout scmGit(branches: [[name: '*/dev']], extensions: [], userRemoteConfigs: [[credentialsId: '28422d1c-e47e-441d-8b46-0da06a4f85bf', url: 'https://github.com/maryamwasimm/Jenkins_assignment.git']])
            }
        }
       
        }    
        }
