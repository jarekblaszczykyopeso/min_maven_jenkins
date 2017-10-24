node {
        stage('Build JAR') {
            // Run the maven build
            sh "mvn clean verify"
            archiveArtifacts 'target/*.jar'
        }
        stage('Publish tests') {
            junit 'target/surefire-reports/*.xml'
      //    jacoco(execPattern: 'target/jacoco-unit/jacoco.exec')
    }
}