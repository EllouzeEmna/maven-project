pipeline {
    agent any
    tools {
        jdk 'JDK19'
    }
    environment {
        JAVA_HOME = 'C:\\Program Files\\Microsoft\\jdk-19'
    }
    stages {
        stage('Compile Stage') {
            steps {
                withMaven(maven: 'maven-399') {
                    bat 'mvn clean compile'
                }
            }
        }
        stage('Testing Stage') {
            steps {
                withMaven(maven: 'maven-399') {
                    bat 'mvn test'
                }
            }
        }
        stage('Install Stage') {
            steps {
                withMaven(maven: 'maven-399') {
                    bat 'mvn install'
                }
            }
        }
    }
}
