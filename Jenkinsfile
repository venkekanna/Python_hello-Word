pipeline {
    agent any

    stages {
        stage('Clone Code') {
            steps {
                git credentialsId: 'github-token', url: 'https://github.com/your-username/python-hello-app.git'
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
