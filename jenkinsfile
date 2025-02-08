pipeline {
    agent {
        docker { image 'maven:3.8.1-adoptopenjdk-11' }
    }
    stages {
        stage('Build') {
            steps {
                sh 'mvn clean compile'  // Only compile, no packaging into JAR
            }
        }
        stage('Run') {
            steps {
                sh 'java -cp target/classes Main'  // Run the compiled Main.java
            }
        }
    }
}
