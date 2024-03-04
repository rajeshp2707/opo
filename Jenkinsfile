pipeline {
    agent any
    tools {
       nodejs "node"
    }
    
    stages {
        stage('Build') {
            steps {
                sh 'npm install'
                
            }
        }
        stage('deploy') {
            steps {
                sh 'npm install -g serve'
                sh 'serve -s build'
            }
        }
        stage('publish') {
              steps {
                  archiveArtifacts artifacts: 'build/'
              }
        }
    }
}
