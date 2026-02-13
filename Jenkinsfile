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
           echo "***************Docker images List************"
           sh "docker images"
           }
         }
      }
}
