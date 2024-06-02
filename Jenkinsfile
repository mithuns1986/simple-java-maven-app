pipeline {
    agent any
    stages {
        stage('Build') {
            agent {
                docker {
                    image 'maven:3.8.7-eclipse-temurin-11'
                    args '-v /root/.m2:/root/.m2' // Optional: mount the local Maven repository
                }
            }
            steps {
                sh 'mvn -B -DskipTests clean package'
            }
        }
    }
}
