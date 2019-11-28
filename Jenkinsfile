pipeline {
	agent { docker 'maven:3.5-alpine' }
	stages {
		stage( 'checkout' ) {
			steps {
				git 'https://github.com/ravigaur06/spring-petclinic'
			}
		}
		stage( 'Build' ) {
			sh 'mvn clean package'
			junit '**/target/surefire-reports/TEST-*.xml'
			}
		}
	}
