pipeline {
    agent any

    environment {
        SONAR_LOGIN = credentials('sqa_419407c3a0bef7f50c4bc1fe27de3ab1fa33388f')
    }

    stages {
        stage('Checkout') {
            steps {
                checkout scm
            }
        }

        stage('SonarQube Analysis') {
            steps {
                script {
                    def scannerHome = tool name: 'SonarScanner', type: 'hudson.plugins.sonar.SonarRunnerInstallation'
                    withSonarQubeEnv('http://localhost:9000/') {
                        sh "${scannerHome}/bin/sonar-scanner"
                    }
                }
            }
        }

        
    }

  
}
