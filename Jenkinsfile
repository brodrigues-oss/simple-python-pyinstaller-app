pipeline {
    agent none 
    stages {
        stage('Build') { 
            agent {
                docker {
                    image 'python:2-alpine' 
                }
            }
            steps {
                sh 'mkdir -pv /var/jenkins_home/workspace'
                sh 'python -m py_compile sources/add2vals.py sources/calc.py' 
            }
        }
    }
}
