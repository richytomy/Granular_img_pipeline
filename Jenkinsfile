pipeline {
    agent  any
    stages {
        stage('Build') {
            steps {
                sh 'magick -version'
            }
        }
        stage('Test') {
            steps {
                sh 'echo test'
            }
            post {
                always {
                    sh 'echo post'
                }
            }
        }
        stage('Deliver') { 
            steps {
                sh 'echo deliver'
                //sh './jenkins/scripts/deliver.sh' 
            }
        }
    }
}
