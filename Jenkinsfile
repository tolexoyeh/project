pipeline {
	agent any 
	stages {
    stage(‘Update’) {
	steps {
        sh "sudo yum install update -y"
	}
	}
	stage (‘Build’) {
	steps {
		sh "sudo yum install npm"
		sh "sudo npm install -g create-react-app@3.4.1"
	}
	}
    stage (‘Initialization’) {
	steps {
		sh "npm init react-app webserver --use-npm"
		sh "npm install react-scripts@3.4.1 -g --silent"
	}
	}
        stage (‘Deploy’) {
	steps {
		sh "cd webserver && npm run build"

	}
	}
}
}
