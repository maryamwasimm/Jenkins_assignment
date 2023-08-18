pipeline {
    agent any

    environment {
        SONAR_LOGIN = credentials('sqa_512309db8bbe8cf1c432b8c5e7dfdc16d78414ae')
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
