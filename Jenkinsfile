pipeline {
    agent { label 'jenkins-slave || jenkins-slave2' }
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
