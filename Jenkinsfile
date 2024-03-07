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
              echo 'asc'
            }
        }
         stage('deploy') {
            steps {
                sh 'npm install'
                sh 'npm run build'
            }
        }
        
       
    }
}
