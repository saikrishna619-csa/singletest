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
				bat 'mvn clean deploy -DmuleDeploy -DskipTests -Dmule.version=4.4.0 -Danypoint.username=Username2021 -Danypoint.password=Password2021 -Denv=Sandbox -Dappname=cicd-demo-1 -Dbusiness=Company -DvCore=Micro -Dworkers=1'
			}
		}
	}
}