pipeline {
	agent any

	environment {
		TEST = 'variable_test'
	}

	stages {
		stage('Test') {
			steps {
				sh 'cat /etc/*release*'
				sh 'echo $TEST'
			}
		}
		
		stage('Deploy - Staging') {
			steps {
				sh 'echo "Staging..."'
			}
		}

		stage('Deploy - Human check') {
			steps {
				input "Does the staging environment look ok?"
			}
		}

		stage('Deploy - Production') {
			steps {
				sh 'echo "Deployment completed successfully."'
			}
		}
	}
}
