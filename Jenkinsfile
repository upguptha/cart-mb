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
        options {
         timeout (time: 300, unit: 'SECONDS')
          }
        inputs {
            message 'Deploying Prod environemnt?',
            ok 'Deploy',
            submitter 'sunisriuppala,bhumihima'

        }
        steps {
            echo "Deploying into Prod Environment"
        }
    }
   
   
   
   
   
   }


}
