pipeline {
	agent any

	stages {
		stage('Compile Stage'){
		  	steps{
				WithMaven(maven : 'maven-3.3.9'){
 					sh 'mvn clean compile'
			}
		}
	}

		stage ('Testing Stage'){
			steps{
				WithMaven(maven : 'maven-3.3.9'){
 					sh 'mvn test'
			}
		}

	}

		stage ('Deployment Stage'){
			steps{
				WithMaven(maven : 'maven-3.3.9'){
 					sh 'mvn deploy'
			}
		}

	}

}
}
