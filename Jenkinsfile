pipeline {
    agent any 


    environment {
        YOUR_SECRET_KEY = 'yourActualSecretKeyHere'
    }

    parameters {
        string(name: 'ciBuildVersion', defaultValue: '1.0.0', description: 'Build version')
        choice(name: 'ciBuildEnv', choices: ['prod', 'dev', 'staging'], description: 'Build environment')
    }

    stages {
        stage('Dependencies') {
            steps {
                echo 'Fetching dependencies...'
                sh 'make deps'
            }
        }

        stage('Test') {
            steps {
                echo 'Running tests...'
              
            }
        }

        stage('Build') {
            steps {
                echo 'Building the binary...'
                
            }
        }

 
         


        stage('Package') {
            steps {
                echo 'Packaging the binary...'
                
            }
        }

        stage('Cleanup') {
            steps {
                echo 'Cleaning up...'
                
            }
        }
    }

    post {
        always {
            echo 'This will always run'
        }
        success {
            echo 'Pipeline completed successfully!'
        }
        failure {
            echo 'Pipeline failed :('
        }
    }
}
