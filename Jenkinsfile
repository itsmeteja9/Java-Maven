@Library('active-shared-libraries') _
pipeline {
    agent {label 'Teja'}

    tools {
        // Install the Maven version configured as "M3" and add it to the path.
        maven "Maven-3.9.9"
    }

    stages {

        stage('code checkout') {
            steps {
                // Get some code from a GitHub repository
                script {
              checkout("https://github.com/itsmeteja9/Test.git", "main")
            }
            }
        }
         
        stage('Build') {
            steps {
                script {
                    mavenbuild()
                }
                // Run Maven on a Unix agent.
                //sh "mvn -Dmaven.test.failure.ignore=true clean package"

                // To run Maven on a Windows agent, use
                
            }


        }
    }
}
