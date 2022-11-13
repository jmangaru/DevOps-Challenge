pipeline {
   agent any
   stages {
       stage('Testing Stage') {
           steps {
               sh """
               echo "Testing"
               """
           }
       }
      stage('Deployment Stage') {
          steps {
               sh """
               echo "Building"
               """
          }
      }
   }
}