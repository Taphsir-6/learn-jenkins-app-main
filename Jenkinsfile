pipeline{
    agent any

    agent {
        docker {
            image 'node:18-alpine'
            args '-v /c/ProgramData/Jenkins/.jenkins/workspace/learn-jenkins-app:/workspace'
        }
    }
    stages {
        stage('Build') {
            steps {
                sh 'npm install'
                sh 'npm run build'
            }
        }
    }
}