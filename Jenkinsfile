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
          		sh 'mvn clean package'
		}
		stage("push to nexus")
		{
		 	echo "pulling code from medium slave "
			stage ("Push Nexus")
			{
  echo " Pushing to nexus Now "
  sh """mvn -U org.apache.maven.plugins:maven-deploy-plugin:2.8.1:deploy-file -DgroupId=in.ashokit \
  -DartifactId=01-maven-web-app \
  -Dversion=1.0-SNAPSHOT \
  -Dpackaging=war \
  -Dfile=target/01-maven-web-app.war \
  -DrepositoryId=nexus_repo-snapshot \
  -Durl=http://3.87.215.204:85/nexus/content/repositories/nexus_repo-snapshot/"""
			
		}

		
}
}
