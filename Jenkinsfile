pipeline {
    agent any
    
    stages {
        stage('Checkout') {
            steps {
            	script {
		        def hasProd = sh(script: 'find prod.go', returnStatus: true)
		        echo hasProd
		        echo 'Hello World!'
                }
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

