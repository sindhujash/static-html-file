pipeline {
    agent any
    stages {
        stage('Archive HTML') {
            steps {
                echo 'Archiving static HTML page...'
                archiveArtifacts artifacts: 'index.html', fingerprint: true
            }
        }
    }
}
