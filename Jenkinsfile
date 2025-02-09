pipeline {
    agent any

    stages {
        stage('Build') {
            steps {
                script {
                    // Run Maven to clean and install the dependencies
                    sh 'mvn clean install'
                }
            }
        }

        stage('Run') {
            steps {
                script {
                    // Run the compiled Main class (assuming package is com.example)
                    sh 'java -cp target/classes com.example.Main'
                }
            }
        }
    }
}
