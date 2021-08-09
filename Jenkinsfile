pipeline {
    agent any

     environment
    {
    PATH="/usr/share/maven:$PATH"
   
    }
    

     stages {
        stage('git') {
            steps {

git branch: 'main', credentialsId: '28a05ef9-3b3c-4466-847a-0a6a0edce8b5', url: 'https://github.com/monisha17068/NewSpringBootProject.git'
}
}
         stage('build') {
            steps {
           sh 'mvn clean install -DskipTests'
        }
    }
         stage('sonar') 
          {
    
        steps
     {
        
   withSonarQubeEnv('sonarqube') {
    sh "mvn sonar:sonar \
  -Dsonar.projectKey=springemp \
  -Dsonar.host.url=http://34.93.225.134:9000 \
  -Dsonar.login=cb6ece6c8202fd3523fca5f01635e2e4647a2d90 "
}
}
 }
  }
}
