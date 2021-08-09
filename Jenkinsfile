pipeline { 
    agent any 
    stages {
        stage('Build') { 
            steps {
                withMaven(maven : 'apache-maven-3.6.3'){
                        sh "mvn clean compile"
                }
            }
        }
        stage('Test'){
            steps {
                withMaven(maven : 'apache-maven-3.6.3'){
                        sh "mvn test"
                }

            }
        }
        stage('Package') {
            steps {
               withMaven(maven : 'apache-maven-3.6.3'){
                        sh "mvn package"
                }

            }
        }
    }
}
