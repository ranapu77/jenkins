 node {
   stage('Git Clone') {
   
		git credentialsId: 'gitlab', url: 'https://github.com/ksproapp/ks.git'
    }
    stage('Maven Clean') {
          sh 'mvn clean'
        }

	stage('Maven Validate') {
          sh 'mvn package'
        }
    stage('Maven Compile') {
          sh 'mvn compile'
        }

	stage('Maven test') {
          sh 'mvn test'
        }
	stage('Maven package') {
          sh 'mvn package'
        }
    stage('Maven Deploy') {
          sh 'mvn deploy'
        }
}
