pipeline {
    agent any
    tools {
        maven 'Maven-3.6.3' 
    }
	stages {
		stage('Gitclone') {
		steps {
		git credentialsId: 'github', url: 'https://github.com/ksproapp/ks.git'
		}
		}
		stage('Maven Clean'){
		steps {
		sh 'mvn clean'
		}
		}
		stage('Maven Compile'){
		steps {
		sh 'mvn compile'
		}
		}
		stage('Maven Test'){
		steps{
		sh 'mvn test'
		}
		}
		stage('Maven Package'){
		steps{
		sh 'mvn package'
		}
		}
		stage('Maven Deploy'){
		steps{
		sh 'mvn deploy'
		}
		}
		}
		
	}
