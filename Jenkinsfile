pipeline{
	agent {
		label 'docker'
		docker {
			image 'maven:3.6.3'} 
		}
	stages{
		stage('Build'){
			// agent {
            // 	docker {
          	// 	label 'docker'
         	// 	image 'maven:3.6.3'}}
			steps{
				sh 'mvn --version'
				echo "Build"
			}
		}
		stage('Test'){
			steps{
				echo "Test"
			}
		}
		stage('Integration Test'){
			steps{
				echo "Integration Test"
			}
		}
	}
	post
	{
		always{
			echo "always"
		}
		success{
			echo "Successful"
		}
		failure{
			echo "Unsuccessful"
		}
	}
	
}