pipeline {
    agent any
    
    stages {
        stage('Build') {
            steps {
                echo 'Building the application...'
                sh 'make -C main'
            }
        }
        
        stage('Test') {
            steps {
                 echo 'Testing the application...'
                 sh 'cd main && ./wrong_executable_name'  // Changed 'hello_exec' to 'wrong_executable_name'
            }
        }
        
        stage('Deploy') {
            steps {
                echo 'Deploying the application...'
                sh 'echo "Deployment completed successfully"'
            }
        }
    }
    
    post {
        success {
            echo 'Pipeline executed successfully!'
        }
        failure {
            echo 'Pipeline failed!'
        }
    }
}
