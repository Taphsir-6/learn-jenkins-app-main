pipeline {
    agent {
        docker {
            image 'node:18-alpine'
            args '-v C:\\ProgramData\\Jenkins\\.jenkins\\workspace\\learn-jenkins-app:/workspace'
        }
    }
    stages {
        stage('Build') {
            steps {
                bat 'npm install'
                bat 'npm run build'
            }
        }
    }
}