pipeline{
    agent any
    tools{
        maven 'maven3'
    }
    stages{
        stage("maven build"){
            when {
                branch 'master'
                steps{
                    sh 'mvn clean package'
                }
            }
            stage("upload artifacts to nexus"){
                when{
                    branch 'develop'
                    steps{
                        echo "upload artifacts to develop"
                    }
                }
                stage("upload artifacts to deploy"){
                    when{
                        branch 'release'
                        steps{
                            echo "upload artifacts "
        }
                    }
                }
    }
        }
    
