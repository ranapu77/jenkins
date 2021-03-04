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
		stage('Maven version'){
		steps {
		sh 'mvn --version'
		}
		}
		stage('Maven Compile'){
		steps {
		sh 'mvn compile'
		}
		}
		stage('SonarQube CodeScan'){
		steps {
		sh 'mvn sonar:sonar -Dsonar.host.url=http://35.232.145.170:9000 -Dsonar.login=6ab753c4df008040f5fe56c3815749f9fad251d2'
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
