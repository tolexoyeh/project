pipeline {
    agent any
    stages {
        stage('Initialization') {
            steps {
                echo 'This is the initialization stage'
            }
	  }
        stage('Input') {
            steps {
                input('Do you want to proceed?')
            }
	  }
        stage('Execution') {
            when {
			  	not {
       	            	branch "main"
				}
		}
            steps {
                echo 'Hello-Execution'
        }
    }
}
