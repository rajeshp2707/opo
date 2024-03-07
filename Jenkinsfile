pipeline {
    agent any
    tools {
       nodejs "node"
    }
    
    stages {
        stage('Build') {
            steps {
              echo 'asc'
            }
        }
         stage('deploy') {
            steps {
                sh 'npm install -g serve'
                sh 'serve -s build'
            }
        }
        
       
    }
}
