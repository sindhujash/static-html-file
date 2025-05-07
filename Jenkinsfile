pipeline {
    agent any
    stages {
        stage('Serve HTML') {
            steps {
                echo 'Serving HTML...'
                sh '''
                    python3 -m http.server 8081 &
                    sleep 10
                '''
            }
        }
    }
}
