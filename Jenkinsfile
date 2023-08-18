pipeline{
    agent any
    stages{
        stage('Checkout'){
            steps{
                checkout scmGit(branches: [[name: '*/dev']], extensions: [], userRemoteConfigs: [[credentialsId: '28422d1c-e47e-441d-8b46-0da06a4f85bf', url: 'https://github.com/maryamwasimm/Jenkins_assignment.git']])
            }
        }
        stage('sonarqube')
        {
            steps{
/opt/sonar-scanner/bin/sonar-scanner \\
  -Dsonar.projectKey=Jenkins_1 \\
  -Dsonar.sources=. \\
  -Dsonar.host.url=http://localhost:9000 \\
  -Dsonar.token=sqp_79b0fa909ed47e680acda162141f945b8b08b0a8'''
            }
        }
       
        }    
        }
