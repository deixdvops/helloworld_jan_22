pipeline {
    agent any
    stages {
        stage (checkout) {
            steps {
              echo "Jenkins checkout the code from github"  
            }
            
        }
        stage (build) {
            steps {
              echo "start the build"  
            }
            
        }
        stage (test) {
            steps {
              echo "Jenkins does unit test"  
            }
            
        }
        stage (deploy) {
            steps {
              echo "Jenkins deploy the artifacts to artifactory"  
            }
            
        }
    }
}
