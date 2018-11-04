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
	echo "Stop Tomcat Server.."
	bat '"C:\\Program Files\\Apache Software Foundation\\Tomcat 8.5\\bin\\Tomcat8.exe" stop'
	echo "Deploy Application into container.."
	bat 'copy /Y %WORKSPACE%\\target\\*.war "C:\\Program Files\\Apache Software Foundation\\Tomcat 8.5\\webapps\\"'
	echo "Start Tomcat Server.."
	bat '"C:\\Program Files\\Apache Software Foundation\\Tomcat 8.5\\bin\\Tomcat8.exe" start'
	}
}
	
	
