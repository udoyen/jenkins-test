pipeline {
    agent none
    stages {
        stage('build') {
    	    agent { docker { image 'maven:3.3.3' } }
            steps {
                sh 'mvn --version'
            }
        }
	stage('node') {
	   agent { docker { image 'node:14-alpine' }}
	   steps {
	       sh 'npm --version'
	   }
	}
	stage('ruby') {
	    agent { docker { image 'ruby' }}
	    steps {
		sh 'ruby --version'
	    }
	}
	stage('python') {
	    agent { docker { image 'python:3.5.1' }}
	    steps {
		sh 'python --version'
	    }
	}
	stage('php') {
	    agent { docker { image 'php' } }
            steps {
                    sh 'php --version'
            }
        }
	stage('golang') {
	    agent { docker { image 'golang' }}
	    steps {
		sh 'go version'
	    }
	}
    }
}


