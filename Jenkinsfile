pipeline {
    agent any
    stages{
        stage('Maven compile'){
            steps{
              sh 'mvn compile'
            }
        }
        stage('Unit test'){
            steps{
              sh 'mvn test'
            }
        }
        stage('maven package'){
            steps{
              sh 'mvn package'
            }
        }
    }
}
