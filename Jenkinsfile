node {
  stage('SCM') {
    check scm
  }
  stage('SonarQube analysis') {
    withSonarQubeEnv('sonarqube') {
      // requires SonarQube Scanner for Maven 3.2+
      sh 'mvn org.sonarsource.scanner.maven:sonar-maven-plugin:3.2:sonar'
    }
  }
}
