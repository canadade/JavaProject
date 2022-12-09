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
                sh 'mvn test'
            }
        }
    }
}