node {
	stage('Clone sources') {
        git url: 'https://github.com/gopilek/gopi_repo.git'
    }
	stage('Maven build') {
        buildInfo = rtMaven.run pom: 'pom.xml', goals: 'clean install'
    }
	}
	
	