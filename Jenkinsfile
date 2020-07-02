# Jenkinsfile (Declarative Pipeline)
# Declerative pipeline starts with "pipeline"
# agent : Where you want to run you job ex: slave nodes
# stages : Build, Test, Deploy.
# steps : What are the commands to execute with in stage    

pipeline {
    agent any 
    stages {
        stage('JOb-1') { 
            steps {
                echo 'Hello Guys!! This is a Job-1' 
            }
        }
        stage('Job-2') { 
            steps {
                echo 'Hello Guys!! This is a Job-2'
            }
        }
        stage('Job-3') { 
            steps {
                echo 'Hello Guys!! This is a Job-3'
            }
        }
        stage('Job-4') { 
            steps {
                echo 'Hello Guys!! This is a Job-3'
            }
        }
        stage('Job-5') { 
            steps {
                echo '$HOSTNAME'
            }
        }
        stage('Job-6') { 
            steps {
                echo 'Hello Guys!! This is a Job-5'
                sh label: '', script: '''whoami'''
            }
        }
        stage('Job-7') { 
            steps {
                echo 'Hello Guys!! This is a Job-6'
                sh label: '', script: '''who'''
            }
        }
    }
}