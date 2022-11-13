pipeline {
    agent any
    stages {
        stage('Testing then Deployment') {
            parallel {
                stage('Testing') {
                    steps {
                        echo 'Testing'
                        sh """
                            echo "Testing"
                        """
                        sh "echo '${WORKSPACE}'"
                        sh """
                            python3 tests/tesot.py
                        """
                    }
                }
                stage('Deployment') {
                    steps {
                        echo 'Deployment'
                        sh """
                            echo "Building"
                        """
                    }
                }
            }
       }
   }
}