Pipeline{
    agent any
    tools {
        jdk 'java-21'
        maven 'maven'
    }
    stages {
        stage('git checkout') {
            steps {
                git url :'https://github.com/Swap1998-nam/DevSecOps-Cal-app/tree/main' branch: 'main'   

            }
        }
        stage('complile') {
            steps {
                sh 'mvn clean complile'
            }
        }
    }


}
