pipeline {
    agent any


    stages{
            stage ('Initialize') {
            steps {
                sh '''
                    echo "PATH = ${PATH}"
                    echo "M2_HOME = ${M2_HOME}"
                '''
            }
            }
            stage('com'){
    def mvnHome = tool name: 'Apache Maven 3.6.0', type: 'maven'
    sh "${mvnHome}/bin/mvn -B -DskipTests clean package"
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
