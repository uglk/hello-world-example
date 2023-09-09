pipeline {
    agent {
        kubernetes{
            yamlFile 'agents.yaml'
        }
    }
    stages {
        stage("git version"){
            steps{
                container("git"){
                sh 'git --version'
            }
            }
        }
        stage("maven version"){
            steps{
                container("git"){
                sh 'mvn --version'
            }
            }
        }
    }
}
