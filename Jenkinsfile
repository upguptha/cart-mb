pipeline {
   agent any
   stages {
      stage ('Build Step') {
         steps {
            echo "Test Mail post job"
         }
      }
   }
   post {
      success {
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
