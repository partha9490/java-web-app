node{
    stage ('checkout code') {
        git branch: 'main', url: 'https://github.com/partha9490/java-web-app.git'

    }
    stage ('build code') {
        sh '/opt/maven/bin/mvn clean package'
    }
    stage ('deploy to tomcat') {
        deploy adapters: [tomcat9(url: 'http://18.140.71.219:8080', credentialsId: 'tomcatcred')], war: '**/*.war'
    }
}