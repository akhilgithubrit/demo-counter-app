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
        stage('build'){
            
            steps{
                 sh 'mvn package'
            }
        }
    }
      
}    
       
