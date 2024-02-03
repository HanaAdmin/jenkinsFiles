pipeline {
    agent any

    stages {
        stage('Hello') {
            steps {
                echo 'Hello World'
            }
        }
        stage('downoalding') {
            steps {
                git branch: 'main', credentialsId: 'GitHub_auth', url: 'https://github.com/HanaAdmin/Application.git'
            }
        }
        
    }
}
