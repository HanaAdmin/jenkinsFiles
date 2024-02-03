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
				
				 sh "ls -al"
            }
        }
		stage('Build') {
            steps {
                
				withMaven(
            // Maven installation declared in the Jenkins "Global Tool Configuration"
            maven: 'MAVEN_3.5'
            
        ) {
          // Run the maven build
          sh "mvn clean package"
        }
				 
            }
        }
        
    }
}
