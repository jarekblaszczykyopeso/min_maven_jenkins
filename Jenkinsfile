node {
        stage('Build JAR') {
            // Run the maven build
            sh "mvn clean verify -Dapplication.version.number=${BUILD_NUMBER} -Dapplication.version.git_branch=${BRANCH_NAME} -Dapplication.version.git_hash=${GIT_COMMIT}"
            archiveArtifacts 'target/*.jar'
        }
        stage('Publish tests') {
            junit 'target/surefire-reports/*.xml'
      //    jacoco(execPattern: 'target/jacoco-unit/jacoco.exec')
    }
}