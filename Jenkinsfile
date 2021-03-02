pipeline {
    agent any
    tools {
        maven 'Maven-3.6.3' 
    }
	stages {
		stage('Gitclone') {
		steps {
		git credentialsId: 'gitlab', url: 'http://34.123.184.116/root/ks.git'
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
