pipeline {
	agent {
        docker {
            image 'maven:3-alpine' 
            args '-v /root/.m2:/root/.m2' 
        }
    }
	stages {
		stage('--push--') {
			steps {
				sh "mvn compile jib:build -DsendCredentialsOverHttp=true -Djib.httpTimeout=0"
			}
		}
	}
}
