pipeline {
	agent any

	stages {
		stage('Compile Stage'){
		  	steps{
				echo 'Compiling...'
 					sh 'mvn clean compile'
			
		}
	}

		stage ('Testing Stage'){
			steps{
				echo 'Testing...'
 					sh 'mvn test'
			
		}

	}

		stage ('Deployment Stage'){
			steps{
				echo 'Deploying...'
 					sh 'mvn deploy'
			
		}

	}

}
}
