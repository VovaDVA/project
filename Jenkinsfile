pipeline {
    agent any
    
    stages {
        stage('Checkout') {
            steps {
                echo 'Hello World!'
            }
        }
    }
    
    post {
        success {
            echo 'Pipeline executed successfully'
        }
        
        failure {
            echo 'Pipeline failed'
        }
    }
}

