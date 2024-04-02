pipeline {
    agent any
    stages {
        stage ('checkout code') {
            steps {
                git branch: 'main', url:'https://github.com/partha9490/java-web-app.git'
            }
        }
        stage ('build code') {
            steps {
                sh '/opt/maven/bin/mvn clean pakage'
            }
        }
        stage ('deploy to tomcat') {
            steps {
                deploy adapters: [tomcat9(url: 'http://18.142.158.200:8080/', credentialsId: 'tomcatcred') ], war: '**/*.war'
            }
        }
    }
}