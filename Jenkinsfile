pipeline {
    agent any
    stages {
        stage ('checkout code') {
            steps {
                git branch:'main', url:'https://github.com/partha9490/java-web-app.git'
            }
        }
        stage ('build code') {
            steps {
                sh '/opt/maven/bin/mvn clean package'
            }
        }
        stage ('deploy to tomcat') {
            steps {
                deploy adapters: [ tomact9('http://47.129.43.73:8080', credentialsId: 'tomcat_id') ], war: '**/*.war'
            }
        }
     
    }
}