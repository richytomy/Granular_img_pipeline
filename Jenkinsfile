pipeline {
    agent  any
    stages {
        stage('Build') {
            steps {
                sh 'magic -version'
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
                //sh './jenkins/scripts/deliver.sh' 
            }
        }
    }
}
