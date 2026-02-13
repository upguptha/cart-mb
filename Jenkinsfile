// i AM COMMENTING THE CODE
pipeline {
// agent any
   agent {
     label 'docker-slave'
  }
  environment {
     DOCKERHUB_CRED = credentials('DOCKERHUB_CREDS')
     dockerhub_repo = "sunisriuppala/jenkinsnginx"
  }
   stages {
      stage ('dockerbuildpush') {
        steps {
           sh "whoami"
           sh "docker pull nginx"
           sh " docker tag nginx ${dockerhub_repo}:v1"
           sh " docker login -u ${DOCKERHUB_CRED_USR} -p ${DOCKERHUB_CRED_PSW}"
           sh "docker push ${dockerhub_repo}:v1"
           }
         }
      }
}
