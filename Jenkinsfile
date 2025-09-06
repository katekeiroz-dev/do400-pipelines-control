pipeline {
    agent {
        node {
            label 'nodejs'
        }
    }

    stages {
        stage('Checkout') {
            steps {
                git branch: 'main', url: 'https://github.com/katekeiroz-dev/do400-pipelines-control'
            }
        }

        stage('Run test') {
            parallel {
                stage('Backend Test') {
                    steps {
                        sh 'node ./backend/test.js'
                    }
                }

                stage('Frontend Test') {
                    steps {
                        sh 'node ./frontend/test.js'
                    }
                }
            }
        }
    }
}

