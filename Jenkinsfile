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
    }
      
}    
       
