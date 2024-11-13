pipeline {
    agent any
    stages {
        stage('Checkout') {
            steps {
                git branch: 'main', url: 'https://github.com/Lamouchi-ale/kaddem.git', credentialsId: 'Nidhal1'
            }
        }

        stage('Run Unit Tests') {
             steps {
                 script {
                     sh 'chmod +x mvnw'
                     sh './mvnw test'
                 }
             }
         }
     
        stage('Build JAR') {
            steps {
                script {
                    sh 'mvn clean package'
                }
            }
        }
    }
}
