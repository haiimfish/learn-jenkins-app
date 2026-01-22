pipeline {
    agent {
        docker {
            image 'node:18'
            reuseNode true
        }
    }

    stages {
        stage('Test npm') {
            agent{
                docker{
                    image 'node:18'
                    reuseNode true
                    }
            }
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