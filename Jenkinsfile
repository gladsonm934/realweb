pipeline{
  agent any

  stages {
    stage('Checkout Code') {
      steps {
        git 'https://github.com/gladsonm934/realweb.git'
      }
    }
    stage('Deploy') {
      steps {
        sh '''
        set -e
        cp -r * /var/www/html/
        '''
      }
    }
  }
  post {
    success {
      echo 'Successfully Completed'
    }
    failure {
      echo 'Failed to up'
    }
  }
}
