node{
    echo "jenkins home directory is ${env.JENKINS_HOME}"
    echo "jenkins job name is ${env.JOB_NAME}"
    echo "jenkins build no is ${env.BUILD_NUMBER}"
    def mavenHome=tool name:'maven3.9.3'
    stage('CheckOutCode')
       {
           git branch: 'development', credentialsId: 'db57f29b-3868-4eed-860c-c42a6cebc619', url: 'https://github.com/Swaroop122/maven-web-application.git'
       }
    stage('Build')
       {
       sh "${mavenHome}/bin/mvn clean package" 
       }
    /*stage('Execute SonarQube Report')
       {
       sh "${mavenHome}/bin/mvn clean sonar:sonar"
       }
     stage('UploadArtifactsIntoNexus')
       {
       sh "${mavenHome}/bin/mvn clean deploy"
       }
     stage('Deploy')
     {
        sshagent(['912b3d2b-8e3e-4681-8209-49196985ddcc'])
        {
      sh "scp -o StrictHostKeyChecking=no target/maven-web-application.war ec2-user@172.31.37.110:/opt/apache-tomcat-9.0.79/webapps/"
    
} 
     }*/
}
