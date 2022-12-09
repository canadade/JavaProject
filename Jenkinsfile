pipeline {
    agent any

    stages {

        stage('Git Checkout'){

            steps{
                git 'https://github.com/canadade/JavaProject.git'
            }
        }
        stage('Unit Testing'){

            steps{
                sh 'mvn test'
            }
        }
    }
}