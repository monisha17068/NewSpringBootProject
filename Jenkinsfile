pipeline {
    agent any

     environment
    {
    PATH="/usr/share/maven:$PATH"
   
    }
    

     stages {
        stage('git') {
            steps {
               git branch: 'main', credentialsId: 'a9b9bb39-55e5-4567-b197-feee34a99d65', url: 'https://github.com/monisha17068/NewSpringBootProject'
            }
        }
        
         stage('build') {
            steps {
           sh 'mvn clean install -DskipTests'
        }
    }
     }}
