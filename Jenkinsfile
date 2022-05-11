pipeline {
    agent any

    stages {
        stage('Hello') {
            steps {
                echo 'Hello World'
            }
        }
        stage('Build') {
            steps {
                echo 'Build Stage'
                sh './mvn clean package'
            }
        }
        stage('SonarTest') {
            steps {
                echo 'Sonar Testing Stage'
            }
        }
    }
}