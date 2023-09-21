pipeline {
	agent any
	
	stages {
	    stage('Checkout') {
	        steps {
			checkout scm			       
		      }}
		stage('Build') {
	           steps {
			  sh '/home/diksha-1/Documents/ExtractFile/apache-maven-3.9.3/bin/mvn install'
	                 }}
		stage('Deployment'){
		    steps {
			
		sh 'cp target/Project1.war /home/diksha-1/Documents/ExtractFile/apache-tomcat-9.0.80/webapps'
		
	}}
	        stage ('slack') {
	         steps {
	                     slackSend baseUrl: 'https://hooks.slack.com/services/', channel: '#nothing', color: 'grren', message: 'welcome', teamDomain: 'Devops'
	                     }}
}}
