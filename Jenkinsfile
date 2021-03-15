pipeline{
	agent any
	stages{
		stage('Git checkout'){
			steps{
				echo "Git checkout successfull";
				git credentialsId: '23cdafa9-ac1a-4d61-a3b4-d35b91f7ac9b', url: 'https://github.com/ZalakBhojani/JenkinsTest'
			}
		}
		stage('Build'){
			steps{
				echo "Build done successfully";
				sh "chmod +x Build.sh";
				sh "./Build.sh"
			}
		}
		stage('Unit test'){
			steps{
				echo "Testing done passed successfully";
				sh "chmod +x Unit.sh";
				sh "./Unit.sh"
			}
		}
		stage('Quality'){
			steps{
				echo "check done successfully";
				sh "chmod +x Quality.sh";
				sh "./Quality.sh"
			}
		}
		stage('Deploy'){
			steps{
				echo "Deployment done successfully";
				sh "chmod +x Deploy.sh";
				sh "./Deploy.sh"
			}
		}
	}

}
