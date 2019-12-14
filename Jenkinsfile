pipeline {
    agent any
    tools {
        maven 'Maven 3.6.3'
		    jdk 'Java8'
    }
    stages {
        stage ('Build') {
            steps {
                sh 'mvn -Dmaven.test.failure.ignore=true clean install package' 
            }
        }
	  }
}
