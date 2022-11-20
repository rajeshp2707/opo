pipeline {
    agent any
    tools {
        nodejs '16.18.1'
    }
    stages {
        stage('build') {
            steps {
                sh 'npm install'
                sh 'npm run build'
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
