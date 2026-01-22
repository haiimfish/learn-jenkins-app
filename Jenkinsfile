pipeline {
    agent {
        docker {
            image 'node:18-alpine' // ใช้ Image นี้ที่มี Node.js มาให้แล้ว
        }
    }
    stages {
        stage('Test npm') {
            steps {
                sh 'npm --version'
                sh 'node --version'
            }
        }
    }
}
