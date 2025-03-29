pipeline {
    agent any
    
    environment {
        GITHUB_URL = 'https://github.com/Blackdeer2/IIC_LABS.git'
    }
    
    stages {
        stage('Clone Repository') {
            steps {
                git branch: 'vysotskyi', url: 'https://github.com/Blackdeer2/IIC_LABS.git'
            }
        }
        
        stage('Update System') {
            steps {
                script {
                    sh 'sudo apt update && sudo apt upgrade -y'
                }
            }
        }
        
        stage('Install Node.js and NPM') {
            steps {
                script {
                    sh 'sudo apt install -y nodejs npm'
                }
            }
        }
        
        stage('Install Dependencies') {
            steps {
                script {
                    sh 'npm install'
                }
            }
        }
        
        stage('Run Dev Server') {
            steps {
                script {
                    sh 'npm run build'
                }
            }
        }
    }
}