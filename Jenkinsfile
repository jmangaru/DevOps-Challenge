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
               python3 --version
               python3 tests/test.py
               """
               sh "python3 tests/test.py"
           }
       }
      stage('Deployment Stage') {
          steps {
               sh "cd '${WORKSPACE}'/"
               sh "sudo virtualenv --python=/usr/bin/python3 venv"
               sh ". venv/bin/activate" 
               sh "pip3 install -r requirements.txt"
               sh "sudo docker-compose up -d --build"
          }
      }
   }
}