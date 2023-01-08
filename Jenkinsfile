node {
	withDockerContainer('node:lts-bullseye-slim') {
		stage('Build') {
			sh 'npm install'	
		}
		stage('Test') {
			sh './jenkins/scripts/test.sh'
		}
	}
}
