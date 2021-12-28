node {
    stage('Git Clone') { 
	  git credentialsId: 'git', url: 'https://github.com/kartikeyapro/ks.git'
    }
    stage('Maven Clean') {
        bat 'mvn clean'
    }
    stage('Maven Validate') {
        bat 'mvn validate'
    }
	 stage('Maven Compile') {
        bat 'mvn compile'
    }
	 stage('Maven Test') {
        bat 'mvn test'
    }
	 stage('Maven Package') {
        bat 'mvn package'
    }
}

