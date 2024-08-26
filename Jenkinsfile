pipeline {
    agent any

    stages {
        stage('Checkout') {
            steps {
                // Checkout code from GitHub
                git 'https://github.com/rajuKollati1/simple-java-project.git'
            }
        }

        stage('Compile') {
            steps {
                // Compile Java code using Jenkins' Java setup
                sh 'javac src/main/java/com/example/App.java'
            }
        }

        stage('Run') {
            steps {
                // Run the Java application
                sh 'java -cp src/main/java com.example.App'
            }
        }

        stage('Test') {
            steps {
                // Run unit tests (adjust if needed for your testing setup)
                sh 'java -cp src/test/java org.junit.runner.JUnitCore com.example.AppTest'
            }
        }
    }
}
