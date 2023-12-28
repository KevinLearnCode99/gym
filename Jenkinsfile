pipeline {
    agent any  // This specifies that any available agent/node can execute this pipeline
    stages {
        stage('Checkout') {
            steps {
                echo 'hello from jenkinsfile'
                git branch: 'main', url: 'https://github.com/KevinLearnCode99/gym.git'
            }
        }
        stage('SonarQube Analysis') {
            steps {
                script {
                    def scannerHome = tool 'SonarQube Scanner'
                    withSonarQubeEnv() {
                        sh "${scannerHome}/bin/sonar-scanner"
                    }
                }

                sshagent(['ssh-agent-docker']) {
                    sh '''
                      scp -o StrictHostKeyChecking=no -r * ubuntu@100.26.171.231:~/website
        '

                    '''
                }
            }
        }
    }
}
