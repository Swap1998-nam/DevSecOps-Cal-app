pipeline {
    agent any

    stages {
        stage('Checkout') {
            steps {
                git branch: 'main',
                    url: 'https://github.com/Swap1998-nam/DevSecOps-Cal-app'
            }
        }
    }
        stage('compile') {
            steps {
                sh 'mvn clean compile'
            }
        }

}



