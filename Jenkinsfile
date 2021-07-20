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
		stage('SonarScan'){
			steps{
				sh 'mvn sonar:sonar -Dsonar.host.url=http://34.70.119.121:9000 -Dsonar.login=c8839c67f75ce2845be9e68d1a7713905b8f7175'
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
				
		
		
		