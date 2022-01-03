node {

    stage('git clone') {
       git credentialsId: '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', url: 'https://github.com/ranapu77/ks.git'
        }
    stage('MVN Clean') {
        sh 'mvn clean'
    }
	    stage('MVN Validate') {
        sh 'mvn validate'
    }
	    stage('MVN Test') {
       sh 'mvn test'
    }
	    stage('MVN Package') {
       sh 'mvn package'
    }
	    stage('MVN Deploy') {
        sh 'mvn deploy'
    }
}
