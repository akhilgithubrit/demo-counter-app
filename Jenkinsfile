pipeline{
    
    agent any
    tools {
          maven 'mvn'
    }

    
    stages {
        
        stage('Git Checkout'){
            
            steps{
                 git branch: 'main', url: 'https://github.com/akhilgithubrit/demo-counter-app.git'
            }
        }
        stage('Unit Testing'){
            
            steps{
                 sh 'mvn test'
            }
        }
        stage('Integration Testing'){
            
            steps{
                 sh 'mvn verify -DskipUnitTests'
            }
        }
        stage('Maveb Build'){
            
            steps{
                 sh 'mvn clean install'
            }
        }
         stage('SonarQube analysis'){
            
            steps{
                 script{
                 withSonarQubeEnv(credentialsId: 'sonar-api') {
                     sh 'mvn clean package sonar:sonar'
                        
                }
            }
           }
        }
    }
      
}    
       
