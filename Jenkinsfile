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
}
}
