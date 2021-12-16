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
                script {
                    app = docker.build("phpwebsite")
                }
            }
            
        }
        
        stage ('Run') {
            steps {
                sh """
                docker run -rm phpwebsite
                """
            }
        }
        
    }
}
