pipeline {
    agent {
        docker {
            image 'node:18-alpine'
            args '-v C:\\ProgramData\\Jenkins\\.jenkins\\workspace\\learn-jenkins-app:/workspace:z --memory 2g --cpus 1.5'
        }
    }
    stages {
        stage('Build') {
            steps {
                script {
                    // Pour Windows, utilisez 'bat' au lieu de 'sh'
                    bat 'npm install'
                    bat 'npm run build'
                }
            }
        }
    }
}