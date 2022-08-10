pipeline {
    agent any

    stages {
        stage('Build') {
            steps {
                echo 'Cloning repo ...'
                // Get some code from a GitHub repository
                git 'https://github.com/SerenaL20/flask-demo.git'

                echo 'Running venv ...'
                // Run venv
                sh "python3 -m venv .venv"

                // Run pip install
                sh "pip3 install -r requirements-dev.txt"
                
                // Run pytest
                sh "python3 -m pytest app-test.py"
            }
        }
    }
}
