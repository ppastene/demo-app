pipeline {
    agent any 
    stages {
        stage('Chekout') {
            steps {
                git branch: 'main', url: 'https://github.com/ppastene/demo-app.git'
            }
        }
        stage('Build') {
            step {
                sh 'mvn clean package'
            }
        }
        stage('Test') {
            step {
                sh 'mvn test'
            }
        }
    }
}
