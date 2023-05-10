pipeline {
  agent any
  environment {
    SCANNER_HOME = tool 'SonarQube'
  }
  stages {
    stage('Test') {
      steps {
        withSonarQubeEnv('SonarQube') {
          sh "${SCANNER_HOME}/bin/sonar-scanner \
            -Dsonar.projectKey=JavaPipeline \
            -Dsonar.projectName=Unreal-Engine-pro2 \
            -Dsonar.sources=. \
            -Dsonar.java.binaries=**/target/classes \
            -Dsonar.exclusions=**/*.java"
        }
      }
    }
  }
}
