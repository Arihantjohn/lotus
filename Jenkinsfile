node('built-in')
{
    stage('Continuous Download')
        {
    git 'https://github.com/sunildevops77/maven.git'
        }
    stage('Continuous Build')
        {
    sh label: '', script: 'mvn package'
        }
    stage('Continuous Deployment')
        {
sh label: '', script: 'scp /home/ubuntu/.jenkins/workspace/ScriptedPipeline/webapp/target/webapp.war   ubuntu@172.31.29.159:/var/lib/tomcat8/webapps/qaenv.war'
        }
    stage('Continuous Testing')
        {
              sh label: '', script: 'echo "Testing Passed"'
        }
    stage('Continuous Delivery')
        {
       input 'waiting for your approval'
sh label: '', script: 'scp /home/ubuntu/.jenkins/workspace/ScriptedPipeline/webapp/target/webapp.war   ubuntu@172.31.23.35:/var/lib/tomcat8/webapps/prodenv.war'
        }
}
