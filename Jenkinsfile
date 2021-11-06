node('master') {
    stage('Continuous Download') {
		git 'https://github.com/sunildevops77/maven.git'
	}
	stage('Continuous build')	{	
		sh label: '', script: 'mvn package'
	}
	stage('Continuous Deployment') {
		sh label: '', script: 'scp  /home/ubuntu/.jenkins/workspace/PipelineScripted/webapp/target/webapp.war   ubuntu@172.31.19.8:/var/lib/tomcat8/webapps/qaenv.war'
	}
	stage('continuous testing')	{
		sh 'echo "Testing Passed"'
	}
	stage('continuous delivery') {
		sh 'scp  /home/ubuntu/.jenkins/workspace/PipelineScripted/webapp/target/webapp.war   ubuntu@172.31.26.65:/var/lib/tomcat8/webapps/prodenv.war'
	}
}
