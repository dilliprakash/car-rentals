pipeline{
    agent any
    tools {
      maven 'maven3'
    }
    

    stages{
        
        stage('Maven Build'){
            when {
                branch 'master'
            }
            steps{
                
                sh "mvn clean package"
            }
        }  
        stage('upload artifact to nexus'){
            when {
                branch 'release'
            }
            steps{
                echo "uploading artifacts to nexus..."
            
            }
       }
    } 
}
