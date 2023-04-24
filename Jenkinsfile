pipeline {
    agent any
       stages {
       stage('Clone') {
           steps {
              git 'https://github.com/letahaphuong/Hello-PHP.git'
           }
       }

    }
    post {
            always {
            sshagent(['ssh-remote']){
                sh 'ssh -o StrictHostKeyChecking=no -l root 45.118.145.149 docker-compose down'
            }
                mail bcc: '', body: 'Hello World!!', cc: '', from: '', replyTo: '', subject: 'Hello World!!', to: 'letahaphuong@gmail.com'
            }
           }
}