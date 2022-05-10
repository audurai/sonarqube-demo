
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
            }
        }
        stage('Deploy') {
            steps {
                echo 'Deploy Stage'
            }
        }
        stage('Test') {
            steps {
                echo 'Test Stage'
            }
        }
        stage('Release') {
            steps {
                echo 'Release Stage'
            }
        }
		stage('Sonarqube_new') {
            steps {
                echo 'Sonarqube new Stage'
				mvn sonar:sonar
				}
            }
        }
        stage('Sonarqube_old') {
            steps {
                echo 'Sonarqube old Stage'
				withSonarQubeEnv(installationName: 'sonarqube-demo-server') {
					sh './mvnw clean org.sonarsource.scanner.maven:sonar-maven-plugin:3.9.0.2155:sonar'
				}
            }
        }
    }
}