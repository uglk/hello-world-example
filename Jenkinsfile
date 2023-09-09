pipeline {
    agent {
        kubernetes{
            yamlFile 'agents.yaml'
        }
    }
    stages {
        // stage("SCM Checkout"){
        //     steps{
        //         container("git"){
        //             git branch: 'main', url: 'https://github.com/uglk/hello-world-example.git'
        //         }
        //     }
        // }
        // stage("Maven Build") {
        //     steps {
        //         container("maven"){
        //             sh 'mvn clean package'
        //             // sh  'mvn clean install -Dmaven.test.skip=true'
        //         }
        //     }
        // }
        stage("git version"){
            container("git"){
                 sh 'git --version'
            }
           
        }
    }
}
