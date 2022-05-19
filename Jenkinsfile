pipeline {
    agent any
    stages {
        stage('build') {
            steps {
                sh 'mvn --version'
                sh 'mvn clean install'
            }
        }
       stage('deploy') {
            steps {
                sh '''rm -rf /var/lib/tomcat9/webapps/*
                    cp target/helloworld.war /var/lib/tomcat9/webapps/ '''
            }
        }
    }
}
