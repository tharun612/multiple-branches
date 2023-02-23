pipeline {
    agent any 
    stages{
        stage("clone"){
            steps { 
                git 'https://github.com/tharun612/hello-world-1.git'
            }    
        }
        stage("build"){
            steps {
                sh 'mvn package'
            }
        }
        stage("deploy"){
            steps {
                deploy adapters: [tomcat9(credentialsId: '668f0060-9193-41bd-9947-f1c1b4b146eb', path: '', url: 'http://18.183.244.158:8080/')], contextPath: null, war: '**/*.war'
            }
        }  
    }
}
