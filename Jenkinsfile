pipeline {
  agent any
  stages {
    stage ('Build') {
       steps {
          echo " Building the application"
       }
    }
  }
  post  {
    //only run this, when the current pipeline or specific stage has success status
    success {
        echo "Post ===================> Success is triggered"
    }
    // only run when the pipeline or stage is failure status
    failure {
        echo " Post ===============> Failure is triggered"
    }
    // This will run irrespective of failure or success ..meaning everytime
    always {
        echo " Post =================> Always is triggered"
    }
  }
}
