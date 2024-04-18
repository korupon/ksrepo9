pipeline {
    agent any

    tools {
          maven 'maven-3.9.5'
    }

    stages {
        stage('Code Clone') {
            steps {
               git branch: 'main', url: 'https://github.com/korupon/ksrepo9.git'
            }
			}
		stage('Maven Version') {
            steps {
               sh 'mvn --version'
            }
			}	
		stage('Maven Clean') {
            steps {
               sh 'mvn clean'
            }
			}
		stage('Maven Validate') {
            steps {
               sh 'mvn validate'
            }
			}
			
			 
				stage('Maven Compile') {
            steps {
               sh 'mvn compile'
            }
			}
		stage('Maven Test') {
            steps {
               sh 'mvn test'
            }
		}
          
		stage('Maven Package') {
            steps {
               sh 'mvn package'
            }
			}			
		stage('Maven Deploy') {
            steps {
               sh 'mvn deploy'
            }
			}			

   }
}
