pipeline {
    agent {
        docker {
            image 'node:18-alpine'
            args '-v /c/ProgramData/Jenkins/.jenkins/workspace/learn-jenkins-app:/workspace -w /workspace --memory 2g --cpus 1.5'
            // Conversion du chemin Windows en format WSL/Linux:
            // C:\ → /c/
            // \ → /
        }
    }
    stages {
        stage('Build') {
            steps {
                script {
                    // Dans un conteneur Linux, utilisez 'sh' au lieu de 'bat'
                    sh 'npm install'
                    sh 'npm run build'
                }
            }
        }
    }
}