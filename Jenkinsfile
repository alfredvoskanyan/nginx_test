pipeline {
    agent any
    stages {
        stage('Build') {
            steps {
                sh ' docker run -it -d -p 9889:80 --name web -v index.html:/usr/share/nginx/html nginx'
                sh '''
                    echo "Multiline shell steps works too"
                    ls -lah
                    curl http://localhost:9889
                '''
            }
        }
    }
}
