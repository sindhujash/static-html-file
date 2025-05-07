pipeline {
    agent any
    stages {
        stage('Serve HTML') {
            steps {
                echo 'Serving HTML using BusyBox httpd...'
                sh '''
                    mkdir -p /tmp/html
                    cp index.html /tmp/html/
                    busybox httpd -f -p 8081 -h /tmp/html &
                    sleep 30
                '''
            }
        }
    }
}
