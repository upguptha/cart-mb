pipeline {
  agent any
  stages {
     stage ('Build') {
        steps {
          echo "Testing MAIL post job"
          }
        }
     }
  
  post {
     success {
         script {
            def subject = "Build status is : ${currentBuild.currentResult}"
            def body = "Build Number is :  ${currentBuild.number}\n" + "Status is : ${currentBuild.currentResult}\n" + "Job URL: ${env.BUILD_URL}"
         }
         mail to: 'srinuuppalakpm+b1@gmail.com',
             subject: subject,
             body: body,
             bcc: '',
             cc: ' ' ,
             from: 'jenkinsstatus@gmail.com',
             replyTo: ''
 
     }

  }
}
