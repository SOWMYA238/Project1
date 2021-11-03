pipeline{
	agent {label 'master'}
	tools{ maven 'M3'}
	stages{
		stage('Checkout'){
			steps{
				git 'https://github.com/SOWMYA238/Project1.git'
			}
		}
		stage(' Build') {
			steps {
				sh 'mvn clean compile'
			}
		}
		stage(' Test') {
			steps {
				sh 'mvn test'
			}
		}
                stage(' Package') {
			steps {
				sh 'mvn package'
                                archiveArtifacts artifacts: 'target/*.jar', followSymlinks: false
			}
		}	
					
	}
}
