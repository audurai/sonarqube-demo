
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
		stage('Sonarqube') {
            steps {
                echo 'Sonarqube new Stage'
				sh './mvn clean install sonar:sonar -Dsonar.login=cbacf5dd948bbb608a432a7b0faa354ff4360ce7'
				}
            }
        }
    }
}