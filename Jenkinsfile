pipeline {
    agent any

    tools {
        // Install the Maven version configured as "M3" and add it to the path.
        maven "Maven"
    }

    stages {
        stage('Build') {
            steps {
                // Get some code from a GitHub repository
                checkout scmGit(branches: [[name: '*/main']], extensions: [], userRemoteConfigs: [[url: 'https://github.com/hbopche/My-WAR-Application.git']])

                // Run Maven on a Unix agent.
                sh "mvn clean install"
            }
        }
      
    }
}
  
