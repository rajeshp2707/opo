pipeline {
    agent any
    tools {
       nodejs "node"
    }
    environment {
            CI = 'true'
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
