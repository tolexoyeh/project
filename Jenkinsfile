pipeline {
    agent any
    stages {
        stage('Initialization') {
            steps {
                echo 'this is the first stage'
            }
	  }
        stage('Input') {
            steps {
                input('Do you want to proceed')
            }
	  }
        stage('Execution') {
            when {
			  	not {
       	            	branch "master"
				}
		}
            steps {
                echo 'Hello'
        }
    }
}
}
