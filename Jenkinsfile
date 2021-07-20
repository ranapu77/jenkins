pipeline {
    agent any
   
    stages {
        stage('Git Clone') {
            steps {
               git branch: 'main', credentialsId: 'gitpass', url: 'https://github.com/ksproapp/myapp.git'
            }
			}
		stage('Maven Version'){
			steps {
				sh 'mvn --version'
				}
				}
		stage('Maven Clean'){
			steps {
				sh 'mvn clean'
			}
			}
		stage('Maven Validate'){
			steps{
				sh 'mvn validate'
				}
				}
		stage('Maven Compile'){
			steps {
			sh 'mvn compile'
			}
			}
		stage('Maven Package'){
			steps {
			sh 'mvn package'
			}
			}
		}
	}	
				
		