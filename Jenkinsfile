node('master')
{
    stage('ContinuousDownload') 
    {
         git 'https://github.com/selenium-saikrishna/maven.git'
    }
    stage('ContinuousBuild') 
    {
         sh label: '', script: 'mvn package'
    }
    stage('ContinuousDeployment')
    {
        sh label: '', script: 'scp /home/ubuntu/.jenkins/workspace/Pipeline/webapp/target/webapp.war ubuntu@172.31.40.249:/var/lib/tomcat8/webapps/testapp.war'
	}
    
}

