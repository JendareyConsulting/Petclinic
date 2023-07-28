pipeline {
    agent any

    tools{
        jdk 'jdk11'
        maven 'maven3'
        }
        
    stages {
        stage('Git Checkout') {
            steps {
                git branch: 'feature-11', url: 'https://github.com/JendareyConsulting/Petclinic.git'
            }
        }
      
        stage('Compile') {
            steps {
                sh "mvn clean compile"
            }
        }
        
        stage('Build') {
            steps {
                sh "mvn clean package"
            }
        }
    }
}
