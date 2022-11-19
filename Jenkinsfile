node ("medium")
{
	stage ("git-clone")
	{
		echo " Pulling changes from branch"
	         checkout([$class: 'GitSCM', branches: [[name: '*/master']], extensions: [], userRemoteConfigs: [[credentialsId: 'github', url: 'https://github.com/Mururadh/Ashokit-project.git']]]) 
	}
	
	  stage ("Maven build code")
		{
          		echo "** Testing the code***"
          		sh 'mvn -v'
		}

		
}
