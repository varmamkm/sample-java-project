pipeline {
    agent any
    
    stages {
        stage('Checkout') {
            steps {
                // Checkout the code from the repository
                git credentialsId: 'your_credentials_id', url: 'https://github.com/varmamkm/sample-java-project.git'
            }
        }
        
        stage('Build') {
            steps {
                // Compile the Java code
                sh 'javac Main.java'
            }
        }
        
        stage('Test') {
            steps {
                // Run tests (if applicable)
                // You can add your test commands here
            }
        }
        
        stage('Deploy') {
            steps {
                // Deployment steps (if applicable)
                // You can deploy your Java application to a server or artifact repository
            }
        }
    }
    
    post {
        success {
            // This block is executed if the pipeline runs successfully
            echo 'Pipeline completed successfully!'
        }
        
        failure {
            // This block is executed if the pipeline fails
            echo 'Pipeline failed!'
        }
    }
}
