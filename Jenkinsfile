pipeline {
    agent any

    stages {
        stage('Build') {
            steps {
                echo 'Building...'
                bat 'mvn clean compile'
            }
        }
        stage('Test') {
            steps {
                echo 'Testing...'
                bat 'mvn test'
            }
        }
        stage('Package') {
            steps {
                echo 'Packaging...'
                bat 'mvn package'
            }
        }
        stage('Deploy') {
            steps {
                echo 'Deploying...'
                bat 'java -cp target/your-app-1.0-SNAPSHOT.jar com.apasoft.ToUpper %param%'
            }
        }
    }
}
