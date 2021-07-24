pipeline {
    agent any
	
    stages {
        stage('gitclone') {
            steps {
                git branch: 'main', credentialsId: 'gitpass', url: 'https://github.com/ksproapp/myapp.git'
            }
        }
		 stage('Maven Version') {
            steps {
                sh 'mvn --version'
            }
			}
         stage('Maven Clean') {
            steps {
                sh 'mvn clean'
            }
			}
         stage('Maven Compile') {
            steps {
                sh 'mvn compile'
            }
			}
		 stage('SonarScan'){
			steps{
				sh 'mvn sonar:sonar -Dsonar.host.url=http://10.128.15.201:9000 -Dsonar.login=c8839c67f75ce2845be9e68d1a7713905b8f7175'
			}
			}	
         stage('Maven Test') {
            steps {
                sh 'mvn test'
            }
			}
         stage('mvn package') {
            steps {
                sh 'mvn package'
            }
			}
	     stage('mvn deploy') {
            steps {
                sh 'mvn deploy'
            }
			}		
		}
    }