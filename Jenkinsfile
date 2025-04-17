pipeline {
    agent {
        docker {
            image 'node:18-alpine'
            args '-v /c/ProgramData/Jenkins:/workspace:z -w /workspace'
        }
    }
    stages {
        stage('Verify') {
            steps {
                bat 'docker --version'
                sh 'ls -la /workspace'
            }
        }
    }
}