pipeline {
    agent any

    stages {
        stage('Checkout') {
            steps {
                // Checkout your source code from version control here
            }
        }
        
        stage('Build') {
            steps {
                // Build your project here
            }
        }
        
        stage('Run Tests') {
            steps {
                // Run your tests here
            }
        }
        
        stage('SonarQube Analysis') {
            steps {
                script {
                    def scannerHome = tool name: 'SonarQubeScanner', type: 'hudson.plugins.sonar.SonarRunnerInstallation'
                    withSonarQubeEnv('SonarQube') {
                        sh "${scannerHome}/bin/sonar-scanner -Dsonar.login=YOUR_GENERATED_TOKEN"
                    }
                }
            }
        }
    }
}
