pipeline {
  agent any
    environment {
      // The following variable is required for a Semgrep Cloud Platform-connected scan:
      SEMGREP_APP_TOKEN = credentials('SEMGREP_APP_TOKEN')
    }
    stages {
      stage('Semgrep-Scan') {
        steps {
          sh 'pip3 install semgrep'
          sh 'semgrep ci'
      }
    }
  }
}
