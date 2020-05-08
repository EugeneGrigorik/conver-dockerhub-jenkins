pipeline {
	agent any
	stages {
		stage('--push--') {
			steps {
				sh "mvn compile jib:build -DsendCredentialsOverHttp=true -Djib.httpTimeout=0"
			}
		}
	}
}
