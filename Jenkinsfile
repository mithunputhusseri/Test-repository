pipeline {
    agent any


    stages{
 
  }
        
        stage('Maven compile'){
            steps{
               def mvnHome = tool name: 'Apache Maven 3.6.0', type: 'maven'
                sh "${mvnHome}/bin/mvn -B -DskipTests clean package"
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
