// i AM COMMENTING THE CODE
pipeline {
   agent any
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
