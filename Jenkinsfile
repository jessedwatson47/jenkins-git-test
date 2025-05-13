pipeline {
    agent any
    stages {
        stage('Build') {
            steps {
                echo "Fetch the source code from Git"
                echo "Compile the code and generate any necessary artefacts using Maven"
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
         stage('Testing') {
            steps {
                echo "Jest: Unit tests"
                echo "Jest: Integration tests"
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
                    echo "CodeSonar: Code quality check success!"
                }
                failure {
                    echo "CodeSonar: Code quality check failed."
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
                echo "Deploying the application to EC2 staging branch "
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
                echo "Selenium: Integration tests"
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
                echo "Deploying code to EC2 production instance"
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
