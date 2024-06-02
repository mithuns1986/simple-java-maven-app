pipeline {
    agent {
        docker {
            image 'maven:3.8.7-eclipse-temurin-11'
            args '-v /root/.m2:/root/.m2' // Add any additional arguments if needed
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
