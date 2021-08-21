node
{
    def mavenHome =tool name :"maven3.8.1"
    stage('checkoutcode')
    {
        git branch: 'development', credentialsId: 'd902a62f-3a46-4a8b-9764-8398014a88ee', url: 'https://github.com/Chowary/maven-web-application.git'
    }
    stage('build')
    {
        sh "${mavenHome}/bin/mvn clean package"
    }
    /*
    stage('test')
    {
        sh "${mavenHome}/bin/mvn sonar:sonar"
    }
    stage('artifactory')
    {
        sh "${mavenHome}/bin/mvn deploy"
    }
    stage('tomcat'){
        sshagent(['4d929059-2e7d-4292-9cd4-d840ef25cd0f']) {
            sh "scp -o StrictHostKeyChecking=no target/maven-web-application.war ec2-user@3.109.59.47:/opt/apache-tomcat-10.0.8/webapps/"
    
       }
    }
    */
}
