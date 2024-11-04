pipeline{
	agent any
	tools {
		maven 'Maven'
	}

	stages {
		stage("build"){
			steps {
				echo 'Step 1 - Compiling App'
				sh 'mvn compile'
			}
		}
		stage("test"){
			steps {
				echo 'Step 2 - Running unit test...'
				sh 'mvn clean test'
			}
		}
		stage("three"){
			steps {
				echo 'Step 3 - Packaging up'
				sh 'mvn package -DskipTests'
			}
		}


	}
	post {
		always {
			echo "This pipeline is complete"
		}
	}
}
