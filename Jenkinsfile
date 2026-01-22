pipeline {
    agent {
        docker {
            image 'node:18'
        }
    }

    stages {
        stage('Test npm') {
            steps {
                sh 'npm --version'
                sh 'node --version'
            }
        }

        stage('Build') {
            steps {
                sh 'npm install'
                sh 'npm run build'
            }
        }
    }
}