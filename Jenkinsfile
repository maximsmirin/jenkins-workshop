pipeline {
    agent any

    stages {
        stage('Prepare') {
            steps {
                echo 'clone'
                git 'https://github.com/maximsmirin/jenkins-workshop.git'
            }
        }
        stage('Build') {
            steps {
             echo 'build'
             sh 'mvn clean package'
	            
            }
        }
        stage('Results') {
            steps {
                echo 'Junit'
                junit '**/target/surefire-reports/TEST-*.xml'
                archiveArtifacts  'target/*.jar'
            }
        }
       
    }
}
