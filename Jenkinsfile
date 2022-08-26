node {
    def app

    stage('Clone repository') {
     
        checkout scm
    }

    stage('Build image') {
        /* This builds the actual image; synonymous to
         * docker build on the command line */
         sudo usermod -aG docker ${USER}

        app = docker.build("getintodevops/hellonode")
    }
}  
