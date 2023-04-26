pipeline{
    agent any

    tools{
    maven "M3"
    }
    stages{
       stage('Build'){
         steps{
             sh "mvn clean compile"
         }
       }

    stages('Test'){
        steps {
            sh "mvn test"
            }
    }
    stages('Deploy'){
            steps {
                sh "mvn heroku:deploy"
                }
        }
    }
}