pipeline {
    agent any

    tools {
        maven 'maven-3.8.4'
    }

    stages {
        stage('Git Clone') {
		    steps {
			git 'https://github.com/ksproapp/ks.git'
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
					
		stage('Maven Validate') {
		    steps {
				sh 'mvn validate'
                    }
					}
					
		stage('Maven Compile') {
		    steps {
				sh 'mvn compile'
                    }
					}
		stage('Sonar Scan'){
			steps {
				sh 'mvn sonar:sonar \
  -Dsonar.host.url=http://34.69.182.82:9000 \
  -Dsonar.login=14b735d9837b6da8b836e6beb280773d4f8b8ced'
					}
					}
		
				stage('Maven Test') {
		    steps {
				sh 'mvn test'
                    }
					}
					
		stage('Maven Package') {
		    steps {
				sh 'mvn package'
                    }
					}
					
		stage('Maven Deploy') {
		    steps {
				sh 'mvn deploy'
                    }
					}
					

     }
}