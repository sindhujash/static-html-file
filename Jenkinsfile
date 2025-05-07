pipeline {
    agent any
    stages {
        stage('Serve HTML using Python HTTP Server') {
            steps {
                echo 'Serving HTML using Python3...'
                sh '''
                    mkdir -p /tmp/html
                    cp index.html /tmp/html/
                    cd /tmp/html
                    nohup python3 -m http.server 8081 &
                    sleep 30
                '''
            }
        }
    }
}
