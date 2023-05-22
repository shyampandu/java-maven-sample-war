pipeline {
    agent any

    stages {
        stage('Hello') {
            steps {
                echo 'Hello World'
		cleanWs()
				
            }
        }
		stage('Checkout code') {
            steps {
                git 'https://github.com/shyampandu/java-maven-sample-war.git'
            }
        }
		stage('clean') {
            steps {
                sh 'mvn clean'
            }
        }
        stage('compile') {
            steps {
                sh 'mvn compile'
            }
        }
		stage('package') {
            steps {
                sh 'mvn package'
            }
        }
    }
	
}

