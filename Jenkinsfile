pipeline {
    agent any
    
    stages {
        stage('Checkout') {
            steps {
            	script {
		        def hasProd = sh(script: 'find -name "prod.go" | wc -l', returnStdout: true)
		        echo "$hasProd"
		        if (hasProd.toInteger() > 0) {
		          sh """
		             chmod u+x deploy.sh
		             ./deploy.sh
		             """
		        } else {
		        	echo "Nothing to deploy"
		        }
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

