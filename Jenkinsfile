pipeline {
    agent {
        node {
            label 'maven'
        }
    }
environment{
    PATH = " /opt/apache-maven-3.9.6/bin:$PATH"
}

    stages {
        stages("build"){
            steps {
                sh 'mvn clean deploy'
            }
        }
    }
}
