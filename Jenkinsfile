pipeline {
    agent any
    tools {
        maven "Maven"   
    }    
    stages {
        stage('Compile-Build-Test') {
            steps {
                sh 'mvn clean package'
            }
        }
        stage('Security Scan'){
            steps{
               probelyScan credentialsId: 'probely', targetId: '31JdHhtSBok9'
                
            }
        }
    }
}
