pipeline {
     triggers {
  pollSCM '* * * * *'
}
    

    agent any
    tools {
  maven 'M2_HOME'
}

   

    stages {
        stage('maven package') {
            steps {
                sh 'mvn clean'
                sh 'mvn install'
                sh 'mvn package'
            }
        }
        stage('test') {
            steps {
                sh 'mvn test'
            }
        }
        stage('docker') {
            steps {
                echo 'docker'
            }
        }
        stage('deploy') {
            steps {
                echo 'deploy'
            }
        }
    }
}
