pipeline{
    agent any
    stages{
stage('Build Docker Image') {
            container('docker') {
              echo 'docker'
              sh "docker build -t username/${image_name}:${image_tag} ."
              sh "docker tag username/${image_name}:${image_tag} ${image_name}:${image_tag}"    
            }
        }
      }
}  
