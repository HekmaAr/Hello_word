pipeline {
    agent any
    tools {
        jdk 'JDK21'
    }
    environment {
        JAVA_HOME = 'C:/Program Files/Java/jdk-21'
    }
    stages {
        stage('Initialize') {
            steps {
                git branch: 'main', url: 'https://github.com/HekmaAr/Hello_word.git'
            }
        }
        stage('Testing Stage') {
            steps {
                withMaven(maven: 'MAVEN-3.9.9') {
                    bat 'mvn test'
                }
            }
        }
        stage('Install Stage') {
            steps {
                withMaven(maven: 'MAVEN-3.9.9') {
                    bat 'mvn install'
                }
            }
        }
    }
}
