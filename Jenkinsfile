pipeline {
    agent {
        docker {
            image 'nginx:alpine'
        }
    }
    stages {
        stage('Serve HTML using Docker NGINX') {
            steps {
                echo 'Serving HTML with Docker NGINX...'
                sh '''
                    mkdir -p html
                    cp index.html html/
                    nohup sh -c "nginx -g 'daemon off;' &" &
                    sleep 30
                '''
            }
        }
    }
}
