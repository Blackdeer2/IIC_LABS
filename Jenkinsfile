pipeline {
    agent any
    stages {
        stage('Checkout') {
            steps {
                git branch: 'vysotskyi', 
                    credentialsId: '1d979e6a-db5a-41c1-99a4-5583779412b6', 
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

