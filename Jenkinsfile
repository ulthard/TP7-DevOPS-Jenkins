pipeline {
    agent any
    tools { 
        maven 'maven-3.8.6' 
        'org.jenkinsci.plugins.docker.commons.tools.DockerTool' 'docker-latest'
    }
    
    stages {
        
        stage("git checkout") {
            steps {
                git url:'https://github.com/ulthard/TP7-DevOPS-Jenkins.git'
            }
        }
        
        stage("Build application") {
            steps {
                sh "mvn clean install"
            }
        }
        
        stage("Unit Test Execution") {
            steps{
                sh "mvn test"
            }
        }
        
        stage("Build the docker image") {
            steps {
                sh "sleep 13"

            }
        }
    }
}
