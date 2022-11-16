properties([parameters([choice(choices: ['master', 'feature-1', 'feature-2'], name: 'branches')])])

// checkout([$class: 'GitSCM', branches: [[name: '*/master']], extensions: [], userRemoteConfigs: [[credentialsId: '62d67b3f-a13b-4116-b035-79fb6713f925', url: 'https://github.com/Mururadh/Ashokit-project.git']]])

node{
	stage ("git-clone")
	{
		echo " Pulling changes from branch $(params.branch)
		git url: "https://github.com/Mururadh/Ashokit-project.git", branch: "$(params.branch)"
	}
}
