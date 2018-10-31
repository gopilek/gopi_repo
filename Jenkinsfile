node {
	stage('Clone sources') {
        git url: 'https://github.com/gopilek/gopi_repo.git'
    }
	stage('Maven build') {
        bat 'C:\Program Files\apache-maven-3.5.4\bin\mvn clean install'
    }
	}
	
	
