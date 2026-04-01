pipeline {
    agent { label 'test' }

    options {
        skipDefaultCheckout(true)
    }


    stages {

        stage('Clone Code') {
            steps {
                git branch: 'main', url: 'https://github.com/fasiuddin007/nodejs-jenkins-demo.git'
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
