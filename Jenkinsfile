pipeline {
    agent any
    tools {
        maven 'Maven'
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
