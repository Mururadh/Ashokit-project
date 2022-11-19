node ("medium")
{
	stage ("git-clone")
	{
		echo " Pulling changes from branch"
	         checkout([$class: 'GitSCM', branches: [[name: '*/master']], extensions: [], userRemoteConfigs: [[credentialsId: 'github', url: 'https://github.com/Mururadh/Ashokit-project.git']]]) 
	}
	
	stage ("maven-build")
		{
		echo "**** Compiling the code*****"
		sh 'mvn -v'
		sh 'mvn clean package'
           	        
		}
	
		
}
