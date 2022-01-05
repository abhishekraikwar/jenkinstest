pipeline{
	agent {docker{ image : 'maven:3.6.3'}}
	stages{
		stage('Build'){
			steps{
				sh "mvn --version"
				echo "Build"
				echo "PATH - $PATH"
				echo "BUILD_NUMBER - $env.BUILD_NUMBER"
				echo "BUILD_ID - $env.BUILD_ID"
				echo "JOB_NAME - $env.JOB_NAME"
				echo "BUILD_TAG - $env.BUILD_TAG"
				echo "BUILD_URL - $env.BUILD_URL"


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