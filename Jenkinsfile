// i AM COMMENTING THE CODE
pipeline {
   agent {
      label 'docker-slave'
   }
   stages {
      stage ('dockerbuildpush') {
        steps {
           sh "docker pull nginx"
           echo "***************Docker images List************"
           sh "docker images"
           }
         }
      }
}
