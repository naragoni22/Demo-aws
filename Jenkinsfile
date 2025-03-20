pipeline {
    agent any

    environment {
        MAVEN_HOME = '/opt/maven'  // Set Maven home
        MAVEN_VERSION = '3.8.4'   // Specify the Maven version you want to install
    }

    stages {
        stage('Install Maven') {
            steps {
                script {
                    // Update package list
                    sh 'sudo apt-get update'

                    // Install Maven
                    sh """
                        sudo apt-get install -y maven
                        echo "Maven installed successfully"
                    """
                    
                    // Optionally, check the Maven version
                    sh 'mvn -version'
                }
            }
        }

        stage('Build Project') {
            steps {
                script {
                    // Running a Maven build command as an example
                    sh 'mvn clean install'
                }
            }
        }
    }

    post {
        always {
            echo 'Cleaning up resources...'
        }
    }
}
