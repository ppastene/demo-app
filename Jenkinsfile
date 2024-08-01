pipeline {
    agent any 
    stages {
        stage('Chekout') {
            steps {
                git branch: 'main', url: 'https://github.com/ppastene/demo-app.git'
            }
        }
        stage('Build') {
            steps {
                sh 'mvn clean package'
            }
        }
        stage('Test') {
            steps {
                sh 'mvn test'
            }
        }
    }
}
