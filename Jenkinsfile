node {
	stage('Clone sources') {
        git url: 'https://github.com/gopilek/gopi_repo.git'
    }
	stage('Maven build') {
       bat 'mvn clean install'
    }
}
	
	
