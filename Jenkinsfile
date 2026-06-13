pipeline {
    agent any

    tools {
        nodejs 'NodeJS18'
    }

    stages {

        stage('Checkout') {
            steps {
                git 'https://github.com/Anusha16-GitH/nodejs-jenkins-demo.git'
            }
        }

        stage('Install Dependencies') {
            steps {
                sh 'npm install'
            }
        }

        stage('Build') {
            steps {
                sh 'npm run build'
            }
        }

        stage('Test') {
            steps {
                sh 'npm test'
            }
        }

        stage('Run') {
            steps {
                sh 'nohup npm start &'
            }
        }
    }
}