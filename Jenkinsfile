pipeline {
    agent any

    tools {
        // Install the Maven version configured as "M3" and add it to the path.
        maven "MAVEN_HOME"
    }

    stages {
        stage('Build') {
            steps {
                // Get some code from a GitHub repository
                git branch: 'main', changelog: false, credentialsId: 'git-ssh', poll: false, url: 'git@github.com:shashank-v-kumar/hello-world.git'

                // To run Maven on a Windows agent, use
                bat "mvn  clean install"
            }

            
        }
    }
}
