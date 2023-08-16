pipeline {
    agent any

    environment {
        PROJECT_DIR = 'C:\\Users\\kean5\\OneDrive\\Desktop\\Degree\\SCC\\Assignment\\spring-petclinic'
    }
    
    //test
    stages {
        stage('Build') {
            steps {
                // Navigate to the project directory
                dir(PROJECT_DIR) {
                    // Execute your build commands
                    sh 'mvn clean install'
                }
            }
        }
        
        stage('Test') {
            steps {
                // Navigate to the project directory
                dir(PROJECT_DIR) {
                    // Execute your test commands
                    sh 'mvn test'
                }
            }
        }
    }
}
