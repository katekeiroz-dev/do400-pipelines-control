pipeline {
    agent {
        node {
            label 'nodejs'
        }
    }
    stages {
	stage('Checkout') {
		steps {
			git branch: 'main', url: 'https://github.com/katekeiroz-dev/do400-pipelines-control.git'
		}
	}
	stage ('Backend Test') {
		sh 'node ./backend/test.js'
        }
	stage ('Frontend Test') {
		sh 'node ./frontend/test.js'
		}
   	 }
     }
}
