pipeline {
	agent any 
	stages {
		stage('Building') {
			steps {
				bat 'mvn clean install -DskipTests'
			}
		}
		stage('Testing') {
			steps {
				bat 'mvn test'
			}
		}
		stage('Deploying') {
			steps {
				bat 'mvn clean deploy -DmuleDeploy -DskipTests -Dusername=suresh736 -Dpassword=Suresh736@   -Denvironment=Sandbox  -Dapplication.name=test-sbi  -Dmule.version=4.3.0   -Dworkers=1 -Dworker.Type=Micro'
			}
		}
	}
}