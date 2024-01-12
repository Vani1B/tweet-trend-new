pipeline {
    agent {
        node {
            label 'maven'
        }
    }

    stages {
        stage("Clone-code"){
            steps {
                git branch: 'main', url: 'https://github.com/Vani1B/tweet-trend-new.git'
            }
        }
    }
}
