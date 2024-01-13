pipeline {
    agent {
        node {
            label 'maven'
        }
    }
    
    stages {
        stage('Clone-code') {
            steps {
                git branch: 'main', url: 'https://github.com/Vani1B/tweet-trend-new.git'
            }
        }
    }
    
    stage('SonarQube analysis') {
    environment {
        scannerHome = tool 'vani-sonar-scanner'
     }
    steps{
    withSonarQubeEnv('vani-sonarqube-server') { // If you have configured more than one global server connection, you can specify its name
      sh "${scannerHome}/bin/sonar-scanner"
    }
    }
  }
}
}

