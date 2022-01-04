pipeline{
	agent {
		label 'docker'
	}
	stages{
		stage('Build'){
			// agent {
            // 	docker {
          	// 	label 'docker'
         	// 	image 'maven:3.6.3'}}
			
			agent {
        docker {
          // Set both label and image
          label 'docker'
          image 'maven:3.6.3'
          args '--name docker-node' // list any args
        }}
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