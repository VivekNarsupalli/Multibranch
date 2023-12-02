node {
   stage('Continuous Download_Master') 
   {
    git branch: 'main', url: 'https://github.com/VivekNarsupalli/My-First-Repo.git'
    }
    stage('Continuous Build_Master')
    {
    sh 'mvn package'
    }
}
		
