pipeline {
    agent any
    stages {
        stage('Build') {
            agent {
                docker {
                    image 'nginx:latest'
                    // Run the container on the node specified at the top-level of the Pipeline, in the same workspace, rather than on a new node entirely:
                    // args '-d -it --entrypoint=/bin/bash -p 8088:80 --name web -v index.html:/usr/share/nginx/html nginx'                }
            }
            steps {
                sh 'ls'
            }
        }
    }
}
