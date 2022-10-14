pipeline {
    agent any 
    stages {
        stage ('hello') {
            steps {
                sh '''
                rm -rf *
                git clone https://github.com/shaikshaestha/sssss.git 
                '''
            }
        }
        stage ('maven_clean') {
            
            steps {
                sh '''
                cd sssss
                mvn clean
                '''
            }
        }
        
        stage ('maven_compile') {
            steps {
                sh '''
                cd sssss
                mvn compile
                '''
            }
        }
        
       
        stage ('maven_test') {
            steps {
                sh '''
                cd sssss
                mvn test install package
                '''
            }
        }
        
    }
}
