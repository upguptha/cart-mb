// i AM COMMENTING THE CODE
pipeline {
   agent any
//   agent {
//     label 'docker-slave'
//  }
  environment {
        DEPLOY_TO = "production"
     }
   stages {
      stage ('production deploy') {
         when {
            environment name: "DEPLOY_TO", value: "production"
         }
        steps {
         echo " Deploying into production"
           }
         }
      }
}
