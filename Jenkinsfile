pipeline {
    agent any
    tools {
        maven 'maven3' 
    }

    stages {
        stage('git checkout') {
            steps {
                git branch: 'main', url: 'https://github.com/amoldataops/FullStack-Blogging-App.git'
            }
        }
        stage('compile') {
            steps {
                sh "mvn compile"
            }
        }
        stage('Test') {
            steps {
                sh "mvn test"
            }
        }
        stage('package') {
            steps {
                sh "mvn package"
            }
        }
    }
}
