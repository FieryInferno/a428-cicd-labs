node {
	withDockerContainer(args:'-p 3000:3000 -v 04c12079dd2ebfeafa6acc78ac1aaf1bdd586101c49f5adc84c44c1dfee4f39f
', image:'node:lts-bullseye-slim') {
		sh 'npm --version'

		stage ('Build') {
			sh 'npm install'
		}
		stage ('Test') {
			sh './jenkins/scripts/test.sh'
		}
	}
}
