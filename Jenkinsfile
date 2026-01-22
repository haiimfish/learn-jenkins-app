pipeline {
    agent {
        docker {
            image 'node:18'
            reuseNode true
            args '-u root'   // ⭐ แก้ permission ตัวต้นเหตุ
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
                sh '''
                rm -rf node_modules package-lock.json
                npm cache clean --force
                npm install
                npm run build
                '''
            }
        }
    }
}
