pipeline {
    agent any

    tools {
        // Install the Maven version configured as "M3" and add it to the path.
        maven "Apache Maven 3.8.1"
    }

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
				
		