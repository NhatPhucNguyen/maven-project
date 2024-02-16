pipeline {
    agent any
    
    tools {
        maven 'MAVEN'
        jdk 'JDK'
    }
    
    stages {
        stage('Checkout') {
            steps {
                git branch: 'main', url: 'https://github.com/NhatPhucNguyen/maven-project'
            }
        }
        stage('Build') {
            steps {
                bat 'mvn -Dmaven.test.failure.ingore=true clean package'
            }
        }
    }
}
