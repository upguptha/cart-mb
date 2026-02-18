pipeline {
   agent any 
   parameters {
       choice (name: 'BuildOnly',
               choices: 'no\nyes',
               description: "This will only build the application"
              )
       choice (name: 'DockerPush',
               choices: 'no\nyes',
               description: "This will build and push to docker repo"
              )
       choice (name: 'deployToDev',
               choices: 'no\nyes',
               description: "This will deploy the app into dev env"
              )
       choice (name: 'deployToTEst',
               choices: 'no\nyes',
               description: "This will deploy the app into Test env"
              )
       choice (name: 'deployToStage',
               choices: 'no\nyes',
               description: "This will deploy the app into Stage env"
              )
       choice (name: 'deployToPord',
               choices: 'no\nyes',
               description: "This will deploy the app into Pord env"
              )
       choice (name: 'ScanOnly',
               choices: 'no\nyes',
               description: "This will do SCAN only"
              )
   }
   stages {
    stage ('Build') {
        when {
            expression {
                params.BuildOnly == 'yes'
            }
        }
        steps {
            echo " Building the project"
        }
    }
    stage ('CodeAnalysis') {
       when {
            expression {
                params.ScanOnly == 'yes'
            }
       }
        steps {
            echo "Running the code analysis"
        }
    }
    stage ('DockerBuildPush') {
       when {
            expression {
                params.DockerPush == 'yes'
            }
       }
        steps {
            echo "Running the code analysis"
        }
    }

    stage ('DeployToDev') {
       when {
            expression {
                params.deployToDev == 'yes'
            }
       }
        steps {
            echo "Deploying into Dev Environment"
        }
    }

    stage ('DeployToTest') {
       when {
            expression {
                params.deployToTEst == 'yes'
            }
       }
        steps {
            echo "Deploying into Test Environment"
        }
    }
    stage ('DeployToStage') {
       when {
            expression {
                params.deployToStage == 'yes'
            }
       }
        steps {
            echo "Deploying into Stage Environment"
        }
    }
    stage ('DeployToPord') {
       when {
           allOf {
             anyOf {
                 expression {
                   params.deployToPord == 'yes'
                 }
               }
             anyOf {
                branch 'production'
             } 
           }
       }
        options {
         timeout (time: 300, unit: 'SECONDS')
          }
        input {
            message 'Deploying Prod environemnt?'
            ok 'Deploy'
            submitter 'sunisriuppala,bhumihima'

        }
        steps {
            echo "Deploying into Prod Environment"
        }
    }
   }
}
