pipeline {
    agent any
    stages {
        stage ('Compile Stage') {

            steps {
                withMaven(maven : 'MAVEN') {
                    git 'https://github.com/Vardhamansankar/sample-junit5-maven.git'
                    sh 'mvn clean compile'
                
            }
            }
        }
        stage ('Testing Stage') {

            steps {
                withMaven(maven : 'MAVEN') {
                    git 'https://github.com/Vardhamansankar/sample-junit5-maven.git'
                    sh 'mvn test'
                
            }
            }
        }
        stage ('Install Stage') {
            steps {
                withMaven(maven : 'MAVEN') {
                  git 'https://github.com/Vardhamansankar/sample-junit5-maven.git'

                    sh 'mvn install'
                
            }
            }
        }
    }
}