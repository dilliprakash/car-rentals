pipeline{
    agent any
    tools{
        maven 'maven3'
    }
    stages{
        stage("maven build"){
            when {
                branch 'master'
            }
                steps{
                    sh 'mvn clean package'
                }
            }
            stage("upload artifacts to nexus"){
                when{
                    branch 'develop'
                }
                    steps{
                        sh 'mvn clean package'
                    }
                }
                stage("upload artifacts to deploy"){
                    when{
                        branch 'release'
                    }
                        steps{
                            sh 'mvn clean package'
        }
                    }
                }
    }
        
    
