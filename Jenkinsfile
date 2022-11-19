node (medium)
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
		docker.image('maven:3.8.6').inside
			{ 
	                 	sh 'pwd'
	                 	echo "Inside Maven container "
	                 	sh 'mvn -v'
	                	sh 'mvn clean package'
           	         }
		}
	
		
}
