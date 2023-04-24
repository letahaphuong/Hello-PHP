pipeline {
    agent any
       stages {
       stage('Clone') {
           steps {
              git 'https://github.com/letahaphuong/Hello-PHP.git'
           }
       }
       post {
        always {

            mail bcc: '', body: 'Hello World!!', cc: '', from: '', replyTo: '', subject: 'Hello World!!', to: 'letahaphuong@gmail.com'
        }
       }
    }
}