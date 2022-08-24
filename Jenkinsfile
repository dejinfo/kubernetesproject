pipeline {
    agent any
              triggers {
                pollSCM '* * * * *'
            }
                stages{
                stage('SCM Checkout') {
            steps{
            git branch: 'master',  url: 'https://github.com/kulareddy86/kubernetesproject/new/master'
            }
        }
      
        stage('build') {
            steps{
            sh 'ls -lrt'
            sh 'docker compose build'
            echo 'docker images build'
            }
        }
        stage('run') {
            steps{
            
            sh 'docker compose up --build'
            echo 'running the containers'
            }
        }
        
}
}
