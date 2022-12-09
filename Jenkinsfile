pipeline {
    agent any

    stages {

        stage('Git Checkout'){

            steps{
                git 'https://github.com/canadade/JavaProject.git'
            }
        }
        stage('UNIT Testing'){

            steps{
                bat 'mvn test'
            }
        }
        stage('Integration testing'){

            steps{
                bat 'mvn verify -DskipUnitTests'
            }
        }
        stage('Maven Build'){

            steps{
                bat 'mvn clean install'
            }
        }
        stage('Sonar quality check'){

            steps{
                script{
                     withSonarQubeEnv(credentialsId: 'sonartoken') {
                      bat 'mvn clean package sonar:sonar'
                 }  
                }
            }
        }
    }
}