pipeline {
    agent {
        node {
            label 'maven'
        }
    }
    environment {
        PATH = "/opt/apache-maven-3.9.6/bin:$PATH"
    }    
    stages {
        stage("build") {
            steps {
                sh 'mvn clean deploy'
            }
        }
        
        stage('SonarQube analysis') {
             environment {
                 scannerHome = tool 'vani-sonar-scanner'
        }
        steps{
           withSonarQubeEnv('vani-sonarqube-server') {
           sh "${scannerHome}/bin/sonar-scanner"
         }
       }
   }
}
}


