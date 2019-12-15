pipeline {
	agent any
	tools {
		maven 'Maven3.6.3'
		jdk 'Java8'
	}
	stages {
		stage ('Build') {
			steps {
				sh 'mvn clean install package' 
			}
		}
		stage ('Artifacts to S3') {
			steps {
				sh 'aws s3 cp target/works-with-heroku-1.0.war s3://milindtech-training-demo-bucket/' 
			}
		}
	}
}
