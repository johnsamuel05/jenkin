pipeline {
    agent any
    
    stages {
        stage('Clone Repository') {
            steps {
                // Clone the repository containing the Java code
                git 'https://github.com/johnsamuel05/jenkin.git'
            }
        }
        stage('Build') {
            steps {
                // Compile the Java code
                script {
                    def javaHome = tool name: 'JDK11', type: 'JDK'
                    env.JAVA_HOME = "${javaHome}"
                    env.PATH = "${javaHome}/bin:${env.PATH}"
                }
                sh 'javac sample.java'
            }
        }
        stage('Test') {
            steps {
                // Run the Java application to verify it works
                sh 'java sample'
            }
        }
}
