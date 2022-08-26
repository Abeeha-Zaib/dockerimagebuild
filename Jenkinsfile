node {
    def app

    stage('Clone repository') {
        /* Let's make sure we have the repository cloned to our workspace */
Environment="JENKINS_LOG=%L/jenkins/jenkins.log"
        checkout scm
    }

    stage('Build image') {
        /* This builds the actual image; synonymous to
         * docker build on the command line */
         sudo usermod -aG docker ${USER}

        app = docker.build("getintodevops/hellonode")
    }
}  
