node (medium)
{
	stage ("git-clone")
	{
		echo " Pulling changes from branch"
		git url: "https://github.com/Mururadh/Ashokit-project.git", branch: "$(params.branch)"
	}
	
	stage ("maven-build")
		{
		echo "**** Compiling the code*****"
		sh 'mvn -v'
		sh 'mvn clean package
		
		}
	
	
	
	
	
}
