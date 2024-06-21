pipeline {
    agent any
    
    stages {
        stage('Clone Repository') {
            steps {
                // Clone the repository containing the Java code
                git branch: 'main', url: 'https://github.com/johnsamuel05/jenkin.git'
            }
        }
        stage('Build') {
            steps {
                // Compile the Java code
                script {
                    def javaHome = tool name: 'JDK9', type: 'JDK'
                    env.JAVA_HOME = "${javaHome}"
                    env.PATH = "${javaHome}/bin:${env.PATH}"
                }
                sh 'javac Hello.java'
            }
        }
        stage('Test') {
            steps {
                // Run the Java application to verify it works
                sh 'java Hello'
            }
        }
    }
}
