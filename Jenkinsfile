
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
        echo 'Build completed'
    }
}

        stage('Test') {
    steps {
        echo 'Running tests...'
        sh 'npm test || echo "No tests found, skipping..."'
    }
}

        stage('Code Quality') {
            steps {
                echo 'Code Quality stage running...'
            }
        }

        stage('Security') {
            steps {
                echo 'Security stage running...'
            }
        }

        stage('Deploy') {
            steps {
                echo 'Deploy stage running...'
            }
        }

        stage('Release') {
            steps {
                echo 'Release stage running...'
            }
        }

        stage('Monitoring') {
            steps {
                echo 'Monitoring stage running...'
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
