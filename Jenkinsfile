pipeline {
    agent any
    tools {
    maven 'M3'
  }

    stages{
            stage ('Initialize') {
            steps {
                sh '''
                    echo "PATH = ${PATH}"
                    echo "M2_HOME = ${M2_HOME}"
                '''
            }
        }
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
