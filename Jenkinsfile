pipeline {
    agent any
    tools {
        maven 'M2_HOME'
    }
    stages {
        stage ('build') {
            steps {
                sh 'mvn clean'
                sh 'mvn install'
                sh 'mvn package'
            }
        }
        stage ('test') {
            steps {
                sh 'mvn test'
               
            }
        }
        stage ('deploy') {
            steps {
               echo 'Deploy step'
                sleep 5
            }
        }
        stage ('docker') {
            steps {
                echo 'image step'
            }
        }
    }
}
