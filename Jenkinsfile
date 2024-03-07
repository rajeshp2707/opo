pipeline {
    agent any
    tools {
       nodejs "node"
    }
    environment {
        CI = 'false'          
    }
    stages {
        stage('Build') {
            steps {
                  sh 'npm install'
            
            }
        }
         stage('deploy') {
            steps {
                echo 'asc'
            }
        }
        
       
    }
}
