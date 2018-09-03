pipeline {
    agent any

    stages {
        stage('Prepare') {
            steps {
                echo 'clone'
                checkout scm
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
