pipeline {
    agent any

    stages {   
        stage('git scm update') {
            steps {
                git url: 'https://github.com/siestageek/nodejs-app.git', branch: 'main'
            }
        }
        stage('docker build') {
            steps {
			sh '''
			docker compose build
			'''
            }
        }
	stage('docker images') {
            steps {
			sh '''
			docker images
			'''
            }
        }
	stage('docker push') {
            steps {
			sh '''
			docker login -u siestageek -p AudvnaWlwl@72
   			docker push zzyzzy/webapp
			'''
            }
        }	    
    }
}
