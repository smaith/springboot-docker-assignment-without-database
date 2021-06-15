pipeline {
    agent any
        tools{
        // Install the Maven version configured as "M3" and add it to the path.
        maven 'maven-3.81'
        }
    stages {
        stage('Build') {
            steps {
                // Get some code from a GitHub repository
                git branch: 'main', url: 'https://github.com/smaith/springboot-docker-assignment-without-database.git'

                // Run Maven on a Unix agent.
                sh "mvn -Dmaven.test.failure.ignore=true clean package"

                // To run Maven on a Windows agent, use
                // bat "mvn -Dmaven.test.failure.ignore=true clean package"
            }
            }
        }
    }
