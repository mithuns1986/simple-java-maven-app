pipeline {
    agent any {
        docker {
            image 'maven:3.8.7-eclipse-temurin-11' 
             
        }
    }
    stages {
        stage('Build') { 
            steps {
                sh 'mvn -B -DskipTests clean package' 
            }
        }
    }
}
