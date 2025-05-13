pipeline {
    agent any
    environment {        
    }
    stages {
        stage('Build') {
            steps {
                echo "Fetch the source code"
                echo "Compile the code and generate any necessary artefacts"
            }
            post {
                success {
                    echo "Build success!"
                }
                failure {
                    echo "Build failed."
                }
            }
        }
         stage('Test') {
            steps {
                echo "Unit tests"
                echo "Integration tests"
            }
            post {
                success {
                    echo "Test success!"
                }
                failure {
                    echo "Test failed."
                }
            }
         }
         stage('Code Analysis') {
            steps {
                echo "Check the quality of the code"
            }
            post {
                success {
                    echo "Code quality check success!"
                }
                failure {
                    echo "Code quality check failed."
                }
            }
         }
        stage('Security Scan') {
            steps {
                echo "OWASP Dependency-Check scan"
            }
            post {
                success {
                    echo "Scan success!"
                }
                failure {
                    echo "Scan failed."
                }
            }
        }
         stage('Deploy') {
            steps {
                echo "Deploying the application to staging branch"
            }
            post {
                success {
                    echo "Deploy success!"
                }
                failure {
                    echo "Deploy failed."
                }
            }
         }
         stage('Integration Tests') {
            steps {
                echo "Integration tests"
            }
            post {
                success {
                    echo "Success!"
                }
                failure {
                    echo "Failed."
                }
            }
         }
         stage('Deploy to Production') {
            steps {
                echo "Deploying code to production"
            }
            post {
                success {
                    echo "Code is now LIVE!"
                }
                failure {
                    echo "Deployment to production failed."
                }
            }
         }
    }
    post {
                success {
                    echo "Pipeline success!"
                }
                failure {
                    echo "Pipeline failed."
                }
            }
}