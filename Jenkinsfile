pipeline {
    agent any
    tools {
        maven 'Maven3' // Asegúrate de tener Maven configurado en Jenkins
        jdk 'JDK17'    // O la versión que uses
    }
    stages {
        stage('Checkout') {
            steps {
                checkout scm
            }
        }
        stage('Test') {
            steps {
                bat 'mvn clean test'
            }
        }
    }
    post {
        always {
             archiveArtifacts artifacts: 'target/karate-reports/**/*.*', fingerprint: true
            junit '**/target/surefire-reports/*.xml'
        }
    }
}
