pipeline {
    agent any  
    parameters {
        string(name: 'PERSON', defaultValue: 'Mr Jenkins', description: 'Who should I say hello to?')

        text(name: 'BIOGRAPHY', defaultValue: '', description: 'Enter some information about the person')

        booleanParam(name: 'TOGGLE', defaultValue: true, description: 'Toggle this value')

        choice(name: 'CHOICE', choices: ['One', 'Two', 'Three'], description: 'Pick something')

        password(name: 'PASSWORD', defaultValue: 'SECRET', description: 'Enter a password')
    }
    stages {
        stage ('EXample')  {
           steps {
            echo "Hello ${params.PERSOSN}"
            echo " Biography: ${params.BIOGRAPHY}"
            echo " Toogle: ${paramas.TOGGLE}"
            echo " selected Choice is: ${params.CHOICE}"
            echo " Password entered is : ${params.PASSWORD}"
           }

        }
    }
}


pipeline {
  agent any
  stages {
    stage ('Build') {
       steps {
          echo " Building the application"
       }
    }
  }
  post {
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

-------------

pipeline {
   agent any 
   stages {
    stage ('Build') {
        steps {
            echo " Building the project"
        }
    }
    stage ('CodeAnalysis') {
        steps {
            echo "Running the code analysis"
        }
    }
    stage ('DockerBuildPush') {
        steps {
            echo "Running the code analysis"
        }
    }

    stage ('DeployToDev') {
        steps {
            echo "Deploying into Dev Environment"
        }
    }

    stage ('DeployToTest') {
        steps {
            echo "Deploying into Test Environment"
        }
    }
    stage ('DeployToStage') {
        steps {
            echo "Deploying into Stage Environment"
        }
    }
    stage ('DeployToPord') {
        steps {
            echo "Deploying into Prod Environment"
        }
    }
   
   
   
   
   
   }


}
