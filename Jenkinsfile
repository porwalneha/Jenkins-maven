pipeline
{
    agent any
    tools {
         maven 'Maven_3.3.9'
          }
    stages{
        stage("GIT-Checkout")
        {
      steps {
    checkout([$class: 'GitSCM', branches: [[name: '*/master']], 
    doGenerateSubmoduleConfigurations: false, 
    extensions: [], 
    submoduleCfg: [], 
    userRemoteConfigs: [[url: 'https://github.com/porwalneha/Jenkins-maven.git']]])
        }
        }
        stage("Build"){
            steps{
               
                sh 'mvn compile'
                sh 'mvn test'
                sh 'mvn package'
                sh 'mvn clean install'
                
            }
        }
}
}
    
    
