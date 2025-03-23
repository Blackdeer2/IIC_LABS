pipeline {
    agent any
    stages {
        stage('Checkout') {
            steps {
                git branch: 'main', 
                    credentialsId: '12345-abcde-67890', 
                    url: 'https://github.com/Blackdeer2/IIC_LABS.git'
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

