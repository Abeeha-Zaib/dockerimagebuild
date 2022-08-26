node {
    def app

    stage('Clone repository') {
     
        checkout scm
    }

    stage('Build image') {
        /* This builds the actual image; synonymous to
         * docker build on the command line */
         sudo usermod -aG docker ${USER}
docker build -t my-image . | tee my-image.build.log
        app = docker.build("getintodevops/hellonode")
    }
}  
