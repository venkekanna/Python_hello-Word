pipeline {
    agent any

    environment {
        PATH = "/usr/local/bin:/usr/bin:/bin"
    }

    stages {
        stage('Install Dependencies') {
            steps {
                sh 'pip3 install -r requirements.txt'
            }
        }

        stage('Run App') {
            steps {
                sh 'python3 app.py &'
            }
        }
    }
}
