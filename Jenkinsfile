pipeline {

    agent any
	tools { 
        maven 'MAVEN' 
        jdk 'JAVA'	

    }
    stages {
        stage('Build') {
            steps {
                bat 'mvn -B -DskipTests clean package'
            }
        }
    
     stage('Sonar Qube analysis') {
            steps {
                bat 'mvn sonar:sonar'
            } 
        }       
    }	
}
