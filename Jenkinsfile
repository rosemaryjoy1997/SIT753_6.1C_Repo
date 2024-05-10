pipeline {
    agent any
    
    stages {
        stage('Build') {
            steps {
                echo 'Stage 1: Build - Build the code using Maven'
                echo 'Tool: Apache Maven'
                // Actual build commands with Maven
            }
            post {
                success {
                    echo 'Build successful!'
                }
                failure {
                    echo 'Build failed!'
                }
            }
        }
        
        stage('Unit and Integration Tests') {
            steps {
                echo 'Stage 2: Unit and Integration Tests - Run unit and integration tests'
                echo 'Tools: JUnit, TestNG, Selenium, Postman'
                // Actual commands for running unit and integration tests
            }
            post {
                success {
            mail to: 'rosemaryjoy97@gmail.com',
                 subject: "Test Success",
                 body: "The Unit and Integration Tests stage  of pipeline ${currentBuild.fullDisplayName} has succeeded."
        }
        failure {
            mail to: 'rosemaryjoy97@gmail.com',
                 subject: "Test Failure",
                 body: "The Unit and Integration Tests stage of pipeline ${currentBuild.fullDisplayName} has failed. Please check logs."
        }
            }
        }
        
        stage('Code Analysis') {
            steps {
                echo 'Stage 3: Code Analysis - Perform code analysis using SonarQube'
                echo 'Tool: SonarQube'
                // Actual commands for code analysis with SonarQube
            }
            post {
                success {
                    echo 'Code Analysis passed successfully!'
                }
                failure {
                    echo 'Code Analysis failed!'
                }
            }
        }
        
        stage('Security Scan') {
            steps {
                echo 'Stage 4: Security Scan - Perform security scan using OWASP Dependency-Check'
                echo 'Tool: OWASP Dependency-Check'
                // Actual commands for security scan
            }
            post {
                success {
            mail to: 'rosemaryjoy97@gmail.com',
                 subject: "Security Scan Success",
                 body: "The Security Scan stage  of pipeline ${currentBuild.fullDisplayName} has succeeded."
        }
        failure {
            mail to: 'rosemaryjoy97@gmail.com',
                 subject: "Security scan Failure",
                 body: "The Security Scan stage of pipeline ${currentBuild.fullDisplayName} has failed. Please check logs."
        }
            }
        }
        
        stage('Deploy to Staging') {
            steps {
                echo 'Stage 5: Deploy to Staging - Deploy the application to a staging server'
                echo 'Tools: Jenkins Pipeline Scripting with SSH, Docker, AWS Elastic Beanstalk, Kubernetes'
                // Actual commands for deployment to staging
            }
            post {
                success {
                    echo 'Deployment to Staging successful!'
                }
                failure {
                    echo 'Deployment to Staging failed!'
                }
            }
        }
        
        stage('Integration Tests on Staging') {
            steps {
                echo 'Stage 6: Integration Tests on Staging - Run integration tests on staging environment'
                echo 'Tools: Selenium, Postman, JMeter'
                // Actual commands for running integration tests on staging
            }
            post {
                success {
                    echo 'Integration Tests on Staging passed successfully!'
                }
                failure {
                    echo 'Integration Tests on Staging failed!'
                }
            }
        }
        
        stage('Deploy to Production') {
            steps {
                echo 'Stage 7: Deploy to Production - Deploy the application to a production server'
                echo 'Tools: Jenkins Pipeline Scripting with SSH, Docker, AWS Elastic Beanstalk, Kubernetes'
                // Actual commands for deployment to production
            }
            post {
                success {
                    echo 'Deployment to Production successful!'
                }
                failure {
                    echo 'Deployment to Production failed!'
                }
            }
        }
    }
    
    post {
        success {
            mail to: 'rosemaryjoy97@gmail.com',
                 subject: "Pipeline Success: ${currentBuild.fullDisplayName}",
                 body: "The pipeline ${currentBuild.fullDisplayName} has succeeded."
        }
        failure {
            mail to: 'rosemaryjoy97@gmail.com',
                 subject: "Pipeline Failure: ${currentBuild.fullDisplayName}",
                 body: "The pipeline ${currentBuild.fullDisplayName} has failed. Please check logs."
        }
    }
}
