pipeline {
    agent any
    
    environment {
        FRONTEND_CREDENTIAL_ID = 'frontend-credentials'
        BACKEND_CREDENTIAL_ID = 'backend-credentials'
    }

    stages {
        stage('Build Frontend') {
            steps {
                script {
                    echo "Building frontend..."
                    // Perform frontend build steps here
                }
            }
        }
        
        stage('Test Frontend') {
            steps {
                script {
                    echo "Testing frontend..."
                    // Perform frontend tests here
                    withCredentials([usernamePassword(credentialsId: FRONTEND_CREDENTIAL_ID, usernameVariable: 'FRONTEND_USERNAME', passwordVariable: 'FRONTEND_PASSWORD')]) {
                        sh "echo Username: $FRONTEND_USERNAME"
                        sh "echo Password: $FRONTEND_PASSWORD"
                    }
                }
            }
        }
        
        stage('Build Backend') {
            steps {
                script {
                    echo "Building backend..."
                    // Perform backend build steps here
                }
            }
        }
        
        stage('Test Backend') {
            steps {
                script {
                    echo "Testing backend..."
                    // Perform backend tests here
                    withCredentials([usernamePassword(credentialsId: BACKEND_CREDENTIAL_ID, usernameVariable: 'BACKEND_USERNAME', passwordVariable: 'BACKEND_PASSWORD')]) {
                        sh "echo Username: $BACKEND_USERNAME"
                        sh "echo Password: $BACKEND_PASSWORD"
                    }
                }
            }
        }
        
        stage('Deploy') {
            steps {
                script {
                    echo "Deploying application..."
                    // Perform deployment steps here
                }
            }
        }
    }
}
