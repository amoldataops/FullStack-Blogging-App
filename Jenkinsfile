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
        stage('compile Do') {
            steps {
                sh "mvn compile"
            }
        }
        stage('Test') {
            steps {
                sh "mvn test"
            }
        }
        stage('packaget') {
            steps {
                sh "mvn package"
            }
        }
    }
}
