pipeline {
	agent any

	stages {
		stage('Compile Stage'){
		  	steps{
				echo 'Compiling...'
 					 'mvn clean compile'
			
		}
	}

		stage ('Testing Stage'){
			steps{
				echo 'Testing...'
 					 'mvn test'
			
		}

	}

		stage ('Deployment Stage'){
			steps{
				echo 'Deploying...'
 					 'mvn deploy'
			
		}

	}

}
}
