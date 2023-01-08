node {
	withDockerContainer(args:'-p 3000:3000', image:'node:lts-bullseye-slim') {
		sh 'npm --version'

		stage ('Build') {
			sh 'npm install'
		}
		stage ('Test') {
			sh './jenkins/scripts/test.sh'
		}
	}
}
