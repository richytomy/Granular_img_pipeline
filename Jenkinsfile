pipeline {
    agent  any
    stages {
        stage('Convert') {
            steps {
                sh 'magick -version'
                sh 'cd scripts'
                sh 'pwd'
                //sh 'cd scripts'
                sh 'chmod +x ./scripts/convert_image.sh'
                sh './scripts/convert_image.sh'
                dir ('/scripts') { 
                sh 'pwd'    
                sh('convert_image.sh')
                  }
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
