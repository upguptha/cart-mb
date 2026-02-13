// i AM COMMENTING THE CODE
pipeline {
//     agent any
   agent {
     label 'docker-slave'
  }
   stages {
      stage ('dockerbuildpush') {
        steps {
           sh "whoami"
           sh "docker pull nginx"
           sh " docker tag nginx sunisriuppala/jenkinsnginx:v1"
           sh "docker push sunisriuppala/jenkinsnginx:v1"
           }
         }
      }
}
