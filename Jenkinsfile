pipeline {
    agent any
    
    stages {
        stage("checkout")
        {
            steps {
                    git branch:'main', url: 'https://github.com/ameerzeya786/demo'   
            }
        }
        stage("build")
        {
            steps {
                 sh "mvn clean install"                
            }

        }
        stage("archive")
        {
            steps {
                archiveArtifacts '**/target/*.jar'
            }
        }
    }

post {
        always {
            sh "echo 'finally block'" 
        }
    }
}
