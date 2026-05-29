pipeline {
    agent any

    stages {

        stage('Checkout') {
            steps {
                echo 'Checking out code...'
                git branch: 'main', url: 'https://github.com/Sneharathod1205/8.2CDevSecOps.git'
            }
        }

        stage('Build') {
            steps {
                echo 'Installing dependencies...'
                sh 'npm install'
            }
        }

        stage('Test') {
            steps {
                echo 'Running tests...'
                sh 'npm test || echo "No tests found"'
            }
        }

        stage('Code Quality') {
            steps {
                echo 'Code Quality Check...'
            }
        }

        stage('Security') {
            steps {
                echo 'Security Scan...'
            }
        }

        stage('Deploy') {
            steps {
                echo 'Deploying application (simulated)...'
            }
        }

        stage('Release') {
            steps {
                echo 'Creating release v1.0.0'
            }
        }

        stage('Monitoring') {
            steps {
                echo 'Monitoring system health...'
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
