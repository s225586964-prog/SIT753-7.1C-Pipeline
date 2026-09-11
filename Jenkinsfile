pipeline {
    agent any

    triggers {
        pollSCM('* * * * *')
    }

    stages {
        stage('Build') {
            steps {
                echo 'Task: Compile and package the application.'
                echo 'Tool: Maven.'
            }
        }

        stage('Unit and Integration Tests') {
            steps {
                echo 'Task: Test individual components and their interactions.'
                echo 'Tools: JUnit and Maven Failsafe.'
            }
        }

        stage('Code Analysis') {
            steps {
                echo 'Task: Analyse code quality and identify maintainability issues.'
                echo 'Tool: SonarQube.'
            }
        }

        stage('Security Scan') {
            steps {
                echo 'Task: Scan dependencies for known security vulnerabilities.'
                echo 'Tool: OWASP Dependency-Check.'
            }
        }

        stage('Deploy to Staging') {
            steps {
                echo 'Task: Deploy the application to an AWS EC2 staging server.'
                echo 'Tool: Ansible.'
            }
        }

        stage('Integration Tests on Staging') {
            steps {
                echo 'Task: Verify application integrations in the staging environment.'
                echo 'Tool: Postman with Newman.'
            }
        }

        stage('Deploy to Production') {
            steps {
                echo 'Task: Deploy the application to an AWS EC2 production server.'
                echo 'Tool: Ansible.'
            }
        }
    }
}
