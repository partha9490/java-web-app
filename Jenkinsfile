pipeline {
    agent {
        node{
            label 'node_partha'
        }
    }   
    stages {
        stage('checkout code') {
            steps {
                git branch: 'main', url: 'https://github.com/partha9490/java-web-app.git'
            }
        }
        stage('build code') {
            steps {
                sh '/opt/maven/bin/mvn clean package'
            }
        }
    }
}
