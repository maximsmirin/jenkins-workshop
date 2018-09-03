node 
    stage ('Preparation'){
        echo 'GIT Clone'
        git clone https://github.com/maximsmirin/jenkins-workshop.git
    }
    stage ('Build'){
        echo 'Clean Package'
	      mvn clean package
    }
    stage ('Results'){
        echo 'Hello World'
    }

}
