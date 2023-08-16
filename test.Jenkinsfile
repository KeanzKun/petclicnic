pipeline {
    agent any

    stages {
        stage('Build') {
            steps {
                // Navigate to the project directory
                dir('C:\Users\kean5\OneDrive\Desktop\Degree\SCC\Assignment\spring-petclinic') {
                    // Execute your build commands
                    sh 'mvn clean install'
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
