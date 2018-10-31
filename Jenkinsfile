node {
	stage('Clone sources') {
        git url: 'https://github.com/gopilek/gopi_repo.git'
    }
	stage('Maven build') {
       bat '''set M2_HOME=C:\\Program Files\\apache-maven-3.5.4
set path=C:\\Program Files\\apache-maven-3.5.4\\bin:%path%;
mvn clean install'''
    }
}
	
	
