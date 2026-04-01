pipeline {
    agent { label 'test' }

    stages {

        stage('Clone Code') {
            steps {
                git 'https://github.com/fasiuddin007/nodejs-jenkins-demo.git'
            }
        }

        stage('Run App') {
            steps {
                sh '''
                node -v || sudo apt install nodejs -y
                node app.js
                '''
            }
        }
    }
}
