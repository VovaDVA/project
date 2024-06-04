pipeline {
    agent any
    
    stages {
        stage('Checkout') {
            steps {
            	script {
		        def hasProd = sh(script: 'find -name "prod.go" | wc -l')
		        if (hasProd > 0) {
		          sh """
		             chmod u+x deploy.sh
		             ./deploy.sh
		             """
		        } else {
		        	echo "Nothing to deploy"
		        }
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

