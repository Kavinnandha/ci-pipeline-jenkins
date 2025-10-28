pipeline {
    agent any

    tools {
        nodejs "node" // Optional if NodeJS is installed globally
    }

    stages {
        stage('Checkout') {
            steps {
                echo 'Cloning repository...'
                git 'https://github.com/Kavinnandha/ci-pipeline-jenkins.git'
            }
        }

        stage('Install Dependencies') {
            steps {
                echo 'Installing dependencies...'
                sh 'npm install'
            }
        }

        stage('Run Tests') {
            steps {
                echo 'Running test cases...'
                sh 'npm test'
            }
        }

        stage('Build') {
            steps {
                echo 'Build successful - ready for deployment'
            }
        }
    }

    post {
        success {
            echo 'CI pipeline executed successfully!'
        }
        failure {
            echo 'Pipeline failed. Check logs.'
        }
    }
}
