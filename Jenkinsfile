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
		stage ('Artifacts to S3') {
			steps {
				sh 'aws s3 cp target/works-with-heroku-1.0.war s3://milindtech-training-demo-bucket/' 
			}
		}
	}
}
