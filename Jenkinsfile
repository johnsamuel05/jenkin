pipeline {
	agent any

	stages {
    	stage('Checkout') {
        	steps {
            	// Checkout code from Git repository
            	git url: 'https://github.com/johnsamuel05/jenkin.git', branch: 'main'
        	}
    	}
   	 
    	stage('Build') {
        	steps {
            	// Example build step, replace with your build commands
            	echo 'Building...'
            	// sh 'make' // Uncomment and replace with your build command
        	}
    	}
   	 
    	stage('Test') {
        	steps {
            	// Example test step, replace with your test commands
            	echo 'Testing...'
            	// sh 'make test' // Uncomment and replace with your test command
        	}
    	}
   	 
    	stage('Deploy') {
        	steps {
            	// Example deploy step, replace with your deploy commands
            	echo 'Deploying...'
            	// sh 'make deploy' // Uncomment and replace with your deploy command
        	}
    	}
	}

	post {
    	success {
        	echo 'Pipeline completed successfully!'
    	}
    	failure {
        	echo 'Pipeline failed!'
    	}
	}
}
