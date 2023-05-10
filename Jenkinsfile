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
            -Dsonar.exclusions=**/*.java \
            -Dsonar.projectKey=jJavaPipeline \
            -Dsonar.projectName=Unreal-Engine-pro2"
        }
      }
    }
  }
}
