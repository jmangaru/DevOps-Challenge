pipeline {
   agent any
   stages {
       stage('Testing Stage') {
           steps {
               cleanWs()
               checkout scm
               sh """
               echo "Testing"
               """
               sh "echo '${WORKSPACE}'"
               sh """
               python --version
               python tests/tjst.py
               """
               sh "python3 tests/test.py"
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