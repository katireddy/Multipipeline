pipeline{
  agent {label 'linux'}
  options {
    buildDiscarder(logRotator(numToKeepStr: '5'))
  }
  stages{
    stage('Hello') {
      steps {
        echo "hello"
      }
    }
    stage('cat Readme.md') {
      when {
        branch "fix-*"
      }
      steps {
        sh '''
        cat README.md
        '''
      }
    }
  }
}
}

