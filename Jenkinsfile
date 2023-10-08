pipeline {
    agent {
        docker {
            image 'maven:3.9.4-eclipse-temurin-11'
            registryUrl
            args '-v /root/.m2:/root/.m2'
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