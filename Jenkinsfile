// Jenkins Declarative Pipeline
pipeline {
<<<<<<< HEAD

    // This pipeline can run on any available Jenkins agent.
    agent any 

    // Using Maven from the 'M2_HOME' installation.
    tools {
        maven 'M2_HOME'
    }

    // Environment variables setup.
    environment {
        ECR_REGISTRY = '518045124624.dkr.ecr.us-east-1.amazonaws.com/devops-repo'
        ECR_CREDENTIAL = 'jenkins-ecr'
    }

    stages {

        // 1. Checkout code from Git.
        stage('Checkout Code') {
            steps {
                git branch: 'main', url: 'https://github.com/deixdvops/helloworld_jan_22.git'
            }
        }

        // 2. Build the code using Maven.
        stage('Build Code') {
            steps {
                sh 'mvn clean package'
            }
        }

        // 3. Test the code using Maven.
        stage('Run Tests') {
            steps {
                sh 'mvn test'
            }
        }

        // 4. Build the Docker image.
        stage('Build Docker Image') {
            steps {
                script {
                    dockerImage = docker.build "${ECR_REGISTRY}:$BUILD_NUMBER"
                } 
            }
        }

        // 5. Push the Docker image to AWS ECR.
        stage('Push to ECR') {
            steps {
                script { 
                    docker.withRegistry("https://${ECR_REGISTRY}", "ecr:us-east-1:${ECR_CREDENTIAL}") {
                        dockerImage.push()
                    }
                }
            }
        }
=======
    agent any
     stages{
      stage('Hello'){
       steps {
         echo "Hello World"
       }
>>>>>>> parent of a3af3d3 (Update Jenkinsfile)
    }
    
    }

}
