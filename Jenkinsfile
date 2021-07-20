node {
    stage('Preparation') { // for display purposes
        // Get some code from a GitHub repository
        git branch: 'main', credentialsId: 'gitpass', url: 'https://github.com/ksproapp/myapp.git'
        // Get the Maven tool.
        // ** NOTE: This 'M3' Maven tool must be configured
        // **       in the global configuration.
        
    }
	stage('mvn version'){
	sh 'mvn --version'
	}
	 
	
    stage('mvn clean') {
        // Run the maven build
         sh 'mvn clean'
    }
      stage('mvn validate') {
        // Run the maven build
       sh  'mvn validate'
    }
  stage('mvn compile') {
        // Run the maven build
       sh 'mvn compile'
    }
  stage('mvn package') {
        // Run the maven build
       sh 'mvn package'
    }
  stage('mvn deploy') {
        // Run the maven build
       sh 'mvn deploy'
    }
}
