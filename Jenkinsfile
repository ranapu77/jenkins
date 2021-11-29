node {
	stage('Git Clone'){
		git 'https://github.com/ksproapp/ks.git'
		}
    stage('Maven Clean') {
      sh 'mvn clean'
    }
    stage('Maven Validate') {
      sh 'mvn validate'
    }
    stage('Maven Compile') {
      sh 'mvn compile'   
    }
	stage('Maven test') {
      sh 'mvn test'
	}
	stage('Maven package'){
	  sh 'mvn package' 
	}
}

