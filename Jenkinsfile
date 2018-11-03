node {
	stage('Clone sources') {
        git url: 'https://github.com/gopilek/gopi_repo.git'
    }
	stage('Maven build') {
	env.JAVA_HOME="${tool 'JDK11'}"
    	env.PATH="${env.JAVA_HOME}/bin:${env.PATH}"
    	bat 'java -version'
      	bat 'mvn clean install'
    }
	stage('Deploy') {
	bat 'copy %WORKSPACE%\\target\\addressbook.war C:\\Program Files\\Apache Software Foundation\\Tomcat 8.5\\webapps\\'
	}
}
	
	
