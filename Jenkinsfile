pipeline {
    agent any

    tools {
        jdk 'java-21'
        maven 'maven'
    }

    stages {
        stage('Checkout') {
            steps {
                git branch: 'main',
                    url: 'https://github.com/Swap1998-nam/DevSecOps-Cal-app'
            }
        }

        stage('Build & Verify') {
            steps {
                sh 'mvn clean verify'
            }
        }

        stage('SonarQube Analysis') {
            steps {
                withSonarQubeEnv('sonarqube') {
                    sh 'mvn sonar:sonar'
                }
            }
        }
    }
}