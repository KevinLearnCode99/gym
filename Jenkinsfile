pipeline {
    agent any  // This specifies that any available agent/node can execute this pipeline

    environment {
        // Define environment variables if needed
        // For example: 
        // MY_VARIABLE = 'some_value'
    }

    stages {
        stage('Checkout') {
            steps {
                echo "hello"
                git branch: 'main', url: 'https://github.com/KevinLearnCode99/gym.git'
            }
        }


    }

  
}

