pipeline {
	agent any
	stages {
		stage("Compile") {
			steps {
				sh "./gradlew compileJava"
			}
			}
		stage("Unit test") {
			steps {
				sh "./gradlew test"
			}
		}
		stage("Code coverage") {
			steps {
				sh "./gradlew test jacocoTestReport"
				sh "./gradlew test jacocoTestCoverageVerification"
			}
		}
	}	
}
