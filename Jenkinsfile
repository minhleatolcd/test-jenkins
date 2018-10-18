pipeline {
	agent any

	environment {
		TEST = 'variable_test'
	}

	stages {
		stage('Test') {
			steps {
				sh 'cat /etc/*release*; echo $TEST'
			}
		}
	}
}
