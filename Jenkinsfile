pipeline {
    agent {
        kubernetes{
            yamlFile 'agents.yaml'
        }
    }
    stages {
        stage("Linting") {
            steps {
                container("maven"){
                    sh 'mvn clean site'
                }
            }
        }
        stage("Maven Version") {
            steps {
                container("maven"){
                    sh 'mvn -version'
                }
            }
        }
    }
}
