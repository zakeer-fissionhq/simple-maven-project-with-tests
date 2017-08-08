pipeline {
    agent any
    tools {
        maven 'maven-3.3.9'
    
    }
    stages {
        stage ('Initialization') {
            steps {
                sh '''
                    
                    echo "PATH = ${PATH}"
                    echo "M2_HOME = ${M2_HOME}"
                '''
            }
        }

        stage ('Building') {
            steps {
                sh 'source /etc/profile'
                sh 'mvn -Dmaven.test.failure.ignore=true install' 
            }
          
        }

          stage ('Compiling') {
            steps {
               sh 'mvn clean compile'
            }
          
        }
    }
}
