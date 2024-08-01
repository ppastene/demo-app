pipeline {
    agent any 
    stages {
        stage('Checkout') {
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
        stage('Sonar Quality Gate') {
            steps {
                sh 'mvn sonar:sonar -Dsonar.projectKey=td_demo_app -Dsonar.host.url=http://192.168.50.145:9000 -Dsonar.login=sqp_2cdd3062a10bbd340f392db6c78b859e361a447c'
            }
        }
    }
}
