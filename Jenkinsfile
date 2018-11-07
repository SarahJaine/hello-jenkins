pipeline {
    agent any
    stages {
        stage('Build') {
            steps {
                sh 'echo "Hello World"'
                sh '''
                    echo "Multiline shell steps works too"
                    ls -lah
                '''
            }
        }
        stage('Health Check') {
            steps {
                timeout(time: 10, unit: 'SECONDS') {
                    sh './health-check.sh'
                }
            }
        }
    }
}