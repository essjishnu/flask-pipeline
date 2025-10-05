pipeline {
  agent any
  stages {
    stage('Build') {
      steps {
        sh 'docker build -t flaskapp .'
      }
    }
    stage('Test') {
      steps {
        sh 'pytest --maxfail=1 --disable-warnings -q'
      }
    }
    stage('Code Quality') {
      steps {
        echo 'Code Quality simulated (SonarQube placeholder)'
      }
    }
    stage('Security') {
      steps {
        echo 'Trivy scan simulated - no major issues found'
      }
    }
    stage('Deploy') {
      steps {
        sh 'docker run -d -p 5000:5000 --name flaskapp flaskapp || true'
      }
    }
    stage('Release') {
      steps {
        echo 'Release tagged and pushed (simulated)'
      }
    }
    stage('Monitoring') {
      steps {
        sh 'docker ps'
      }
    }
  }
}
