pipeline {
    agent any 
    stages {
        stage('Clone and Clean') { 
            steps {
            sh " rm -r *"
            sh "git clone https://github.com/dedubey/my-app.git"
            sh "mvn clean -f my-app"
            }
        }
        stage('Test') { 
            steps {
                sh "mvn test -f my-app" 
            }
        }
        stage('Deploy') { 
            steps {
                sh "mvn package -f my-app" 
            }
        }
    }
}
