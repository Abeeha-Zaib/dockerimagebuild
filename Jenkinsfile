pipeline{
    agent any
    stages{
stage('Build Docker Image') {
    steps{
            container('docker') {
              echo 'docker'
              sh "docker build -t username/${image_name}:${image_tag} ."
                sh "docker tag username/${image_name}:${image_tag} ${image_name}:${image_tag}"   } 
            }
        }
        tage('publish') {
  steps {
    script {
      image.push rev
      image.push 'latest'
    }
  }
}


      }
}  
