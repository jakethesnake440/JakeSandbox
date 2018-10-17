pipeline {
  agent any
  stages {
    stage('') {
      steps {
        bat(script: 'build1', returnStatus: true, returnStdout: true)
        emailext(subject: 'Pipeline executed successfully: \'${currentBuild.fullDisplayName}\'', body: 'The full build information can be seen here: \'${env.BUILD_URL}\'', attachmentsPattern: 'SCMwizardZip\\\\*', mimeType: 'text/html', to: 'jake.wallace@hyland.com, ariel.koiman@hyland.com')
      }
    }
  }
}