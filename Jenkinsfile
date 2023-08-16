pipeline {
    agent any

    environment {
        PROJECT_DIR = 'C:\\Users\\kean5\\OneDrive\\Desktop\\Degree\\SCC\\Assignment\\spring-petclinic'
        MAVEN_HOME = 'C:\\Program Files\\apache-maven-3.8.8'  // Replace with your Maven installation path
    }

    stages {
        stage('Checkout') {
            steps {
                // Obtains the source code from the Source Code Management system
                checkout scm
            }
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

        stage('Build') {
            steps {
                dir(PROJECT_DIR) {
                    // Execute your build commands
                    bat "${MAVEN_HOME}\\bin\\mvn install"
                }
            }
        }
        
        stage('Test') {
            steps {
                dir(PROJECT_DIR) {
                    // Execute your test commands
                    bat "${MAVEN_HOME}\\bin\\mvn test"
                }
            }
        }
    }
    
    post {
        always {
            // This section can contain tasks you want to always execute regardless of build outcome
        }
        
        success {
            echo 'Build and Test stages completed successfully!'
        }
        
        failure {
            echo 'There was a failure during one of the stages!'
        }
    }
}
