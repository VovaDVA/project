pipeline {
    agent any
    
    stages {
        stage('Checkout') {
            steps {
                def hasProd = sh 'find prod.go'
                echo $hasProd
                echo hasProd
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

