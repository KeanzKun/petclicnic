pipeline {
    agent any

    environment {
        PROJECT_DIR = 'C:\\Users\\kean5\\OneDrive\\Desktop\\Degree\\SCC\\Assignment\\spring-petclinic'
    }
    
            stage('Format Code') {
            steps {
                dir(PROJECT_DIR) {
                    script {
                        // Automatically format the code
                        bat "${MAVEN_HOME}\\bin\\mvn spring-javaformat:apply"
                    }
                }
            }
        }
        
    stages {
        stage('Build') {
            steps {
                // Navigate to the project directory
                dir(PROJECT_DIR) {
                    // Execute your build commands
                    bat 'mvn install'
                }
            }
        }
        
        stage('Test') {
            steps {
                // Navigate to the project directory
                dir(PROJECT_DIR) {
                    // Execute your test commands
                    bat 'mvn test'
                }
            }
        }
    }
}
