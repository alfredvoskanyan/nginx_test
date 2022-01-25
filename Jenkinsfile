pipeline {
    agent any
    stages {
        stage('Build') {
            steps {
                sh ' docker run -it -d -p 9889:80 --name web -v ~/site-content:/usr/share/nginx/html nginx'
            }
        }
        stage('Test Web Page') {
            steps {
                sh '''
                    echo "Multiline shell steps works too"
                    ls -lah
                    curl http://localhost:9889
                    curl --write-out '%{http_code}' --silent --output /dev/null http://localhost:9889
                    docker stop web
                    docker rm web
                '''
            }
        }       
    }
}
