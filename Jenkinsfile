pipeline {
    agent any

    environment {
        PROJECT_DIR = 'C:\Users\kean5\OneDrive\Desktop\Degree\SCC\Assignment\spring-petclinic'
    }

    stages {
        stage('Build') {
            steps {
                // Navigate to the project directory
                dir('C:\Users\kean5\OneDrive\Desktop\Degree\SCC\Assignment\spring-petclinic') {
                    // Execute your build commands
                    sh 'mvn install'
                }
            }
        }

        stage('Test') {
            steps {
                // Navigate to the project directory
                dir('C:\Users\kean5\OneDrive\Desktop\Degree\SCC\Assignment\spring-petclinic') {
                    // Execute your test commands
                    sh 'mvn test'
                }
            }
        }
    }
}