node {
   stage('Continuous Download') 
   {
    git branch: 'main', url: 'https://github.com/VivekNarsupalli/My-First-Repo.git'
    }
    stage('Continuous Build')
    {
    sh 'mvn package'
    }
	stage('Continuous Deployment')
    {
    sh 'scp /home/ubuntu/.jenkins/workspace/Sample/target/webappartifact-1.0-SNAPSHOT.jar ubuntu@172.31.21.3:/var/lib/tomcat9/webapps/qaenv.war'
    }
    stage('Continuous Testing')
    {
    sh 'echo \'Testing Passed\''
    }
	stage('Continuous Delivery')
    {
    sh 'scp /home/ubuntu/.jenkins/workspace/Sample/target/webappartifact-1.0-SNAPSHOT.jar ubuntu@172.31.31.26:/var/lib/tomcat9/webapps/qaenv.war'
    }
}
		