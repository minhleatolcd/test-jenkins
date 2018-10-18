pipeline {
	agent any

	environnement {
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
