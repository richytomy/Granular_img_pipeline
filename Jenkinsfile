pipeline {
    agent  any
    stages {
        stage('Convert') {
            steps {
                sh 'magick -version'
                sh './scripts/convert_image.sh'
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
