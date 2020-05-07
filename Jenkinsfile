pipeline {
	agent any
	stages {
		stage('--push--') {
			steps {
				bat "mvn compile jib:build -DsendCredentialsOverHttp=true -Djib.httpTimeout=0"
			}
		}
	}
}