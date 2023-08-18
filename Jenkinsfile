pipeline {
    agent {
        kubernetes{
            yamlFile 'application/agents.yaml'
        }
    }
    stages {
        stage("Git Version") {
            steps {
                container("git"){
                    sh 'git --version'
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
