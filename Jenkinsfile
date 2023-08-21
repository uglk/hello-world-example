pipeline {
    agent {
        kubernetes{
            yamlFile 'agents.yaml'
        }
    }
    stages {
        // stage("Linting") {
        //     steps {
        //         container("maven"){
        //             sh 'mvn clean site'
        //         }
        //     }
        // }
        stage("SCM Checkout"){
            steps{
                container("git"){
                    git branch: 'main', url: 'https://github.com/uglk/hello-world-example.git'
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
