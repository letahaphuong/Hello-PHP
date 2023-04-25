pipeline {
    agent any
       stages {
       stage('Clone') {
           steps {
              git 'https://github.com/letahaphuong/Hello-PHP.git'
           }
       }
       stage('Test'){
                    steps {
                     sh(script: 'dotnet test -l:trx || true')
                    }
                }
       stage('Deploy') {
                    steps {
                        sh 'make publish'
                    }
                }

    }
    post {
            always {

                mail bcc: '', body: 'Hello World!!', cc: '', from: '', replyTo: '', subject: 'Hello World!!', to: 'letahaphuong@gmail.com'
            }
           }
}