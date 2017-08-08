pipeline {
    agent any
    tools {
        maven 'maven-3.3.9'
    
    }
    stages {
        stage ('Initialization') {
            steps {
                sh '''
                    export "PATH=/usr/lib/jvm/jre-1.8.0-openjdk:${PATH}"
                    echo "PATH = ${PATH}"
                    echo "M2_HOME = ${M2_HOME}"
                '''
            }
        }

        stage ('Building') {
            steps {
                sh '''
                    export "JAVA_HOME=/usr/lib/jvm/jre-1.8.0-openjdk"
                    export "PATH=${JAVA_HOME}:${PATH}"
                '''
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
