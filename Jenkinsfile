pipeline {
  agent any
  stages {
     stage ('Build') {
        steps {
          echo "Testing MAIL post job"
          }
        }
     }
  }
  post {
     success {
         script {
            def Subject = "Build status is : ${currentBuild.currentResult}"
            def body = "Build Number is :  ${currentbuild.number}\n" + "Status is : ${currentBuild.currentResult}\n" + "Job URL: ${env.BUILD_URL}"
         }
         mail to: 'srinuuppalakpm+b1@gmail.com',
             subject: "Jenkins job status",
             body: "Build is Success",
             bcc: '',
             cc: ' ' ,
             from: 'jenkinsstatus@gmail.com',
             replyTo: ''
 
     }

  }
}
