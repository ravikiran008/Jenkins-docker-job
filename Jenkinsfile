// This pipeline is used to build a docker image and push the image to the Dockerhub

pipeline {
    agent {
  label 'jenkins-slave-1'
}
    stages {
        stage('CheckOut-Git') { 
            steps {
                echo 'Hello Guys!! Thios step copies code form git hub to jenkins workspace' 
                checkout([$class: 'GitSCM', branches: [[name: '*/master']], doGenerateSubmoduleConfigurations: false, extensions: [], submoduleCfg: [], userRemoteConfigs: [[url: 'https://github.com/ravikiran008/Jenkins-docker-job.git']]])
            }
        }
        stage('Build-Docker-Image') { 
            steps {
                echo 'Hello Guys!! This Stage Builds the Docker Image'
                sh label: '', script: 'docker build -t  ravikirantht/jenkins-image:$BUILD_NUMBER .'
            }
        }
        stage('Docker-Login') { 
            steps {
                echo 'Hello Guys!! Tghis step will login to docker hub'
                sh label: '', script: 'docker login -u ravikirantht -p aws123'
            }
        }
        stage('Push Docker Image') { 
            steps {
                echo 'Hello Guys!! This Job will push the Docker Image to Docker hub'
                sh label: '', script: 'docker push ravikirantht/jenkins-image:$BUILD_NUMBER'
            }
        }
        }
    }