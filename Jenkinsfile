pipeline {
    agent any
    stages {
        stage('Serve HTML using Docker') {
            steps {
                script {
                    sh '''
                        mkdir -p html
                        cp index.html html/

                        docker run --rm -d -p 8081:80 \
                            -v $PWD/html:/usr/share/nginx/html:ro \
                            --name static-server nginx

                        sleep 30
                    '''
                }
            }
        }
    }
}
