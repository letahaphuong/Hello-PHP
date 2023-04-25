pipeline {
    agent any
       stages {
       stage ('Git Checkout') {
         steps {
             git branch: 'main', url: 'https://<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>@https://github.com/letahaphuong/Hello-PHP.git'
            }
         }
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