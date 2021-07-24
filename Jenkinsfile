pipeline {

agent {
    node {
      label 'master'
    }
    node {
        stage('SCM') {
            checkout scm
        }
    }
  
      tools {
        jdk 'jdk-8.221'
        maven 'default maven'
    }
    
    stages {
        
     stage('Maven version') {
            steps {
                echo "Hello, Maven"
                sh "mvn --version" 
            }
        }
        
        stage('Stage 1') {
            steps {
                sh 'mvn clean package'
            }
            
        }
        
        stage('Stage 2') {
            steps {
                echo 'Stage2 Hello world!'  
                echo  'Stage2 $date'
            }
            
        }
        
        
        stage('Stage 3') {
            steps {
                echo 'Wel come to Stage3 '  
                echo  'Stage3 '
            }
            
        }
        
    }
}
