pipeline {
    agent any

    stages {
        stage('Hello') {
            steps {
                echo 'Hello World'
            }
        }
        stage('checkout') {
            steps {
               checkout scmGit(branches: [[name: '*/master']], extensions: [], userRemoteConfigs: [[url: 'https://github.com/shyampandu/java-maven-sample-war.git']])
            }
        }
         stage('clean and compile') {
            steps {
              sh 'mvn clean install compile'
            }
        }
		stage('package') {
            steps {
              sh 'mvn package'
            }
        }
		
    }
}
