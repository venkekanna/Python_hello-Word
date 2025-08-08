pipeline {
    agent any

    environment {
        APP_DIR = 'python-hello'
    }

    stages {
        stage('Clone Code') {
            steps {
                git url: 'https://github.com/venkekanna/Python_hello-Word.git'
            }
        }

        stage('Install Dependencies') {
            steps {
                sh 'pip3 install -r requirements.txt'
            }
        }

        stage('Run App') {
            steps {
                sh 'nohup python3 app.py &'
            }
        }
    }
}
