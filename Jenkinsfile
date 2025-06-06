pipeline{
	agent any
	tools{
		jdk 'jdk'
		maven 'maven'
	}
	stages{
		stage('Checkout'){
			steps{
				git branch: 'master', url: 'https://github.com/Megharaj2004/Mapp'
			}
		}
		stage('Build'){
			steps{
				sh 'mvn clean package'
			}
		}
		stage('Run'){
			steps{
				sh 'java -cp target/Mapp-1.0-SNAPSHOT.jar com.example.App'
			}
		}
	}
}
