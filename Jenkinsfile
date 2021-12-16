pipeline {
    agent any
    stages {
        stage('Checkout from Github') {
            steps {
                checkout scm
            }    
        }
        
        stage ('Build docker image') {
            steps {
                app = docker.build("phpwebsite")
            }
        }
        
        
    }
}
