pipeline {
   agent any
   stages {
      stage ('Build') {
        steps {
           echo 'Build process will be done in this step'
           }
         }
      stage ('Sonar') {
        steps {
           echo 'code quality process will be done in this step'
           }
         }
      stage ('Docker') {
        steps {
           echo 'IMAGE preparation and push the image to repository will be done in this stage'
           }
         }
      stage ('Deployment') {
        steps {
           echo 'Deployment process will be will be done in this stage'
           }
         }
     }
}
