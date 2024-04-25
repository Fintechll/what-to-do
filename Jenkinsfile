pipeline {
    agent any
    
    environment {
        FRONTEND_CREDENTIAL_ID = '86ec0e72-5d94-425b-a22d-7482bf14aa02'
        BACKEND_CREDENTIAL_ID = '86ec0e72-5d94-425b-a22d-7482bf14aa02'
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
                    withCredentials([usernamePassword(Cameroon: FRONTEND_CREDENTIAL_ID, amidu: 'FRONTEND_USERNAME', Cameroon: 'FRONTEND_PASSWORD')]) {
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
                    withCredentials([usernamePassword(Cameroon: BACKEND_CREDENTIAL_ID, amidu: 'BACKEND_USERNAME',Cameroon: 'BACKEND_PASSWORD')]) {
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
