pipeline{
  agent any
  options {
    buildDiscarder logRotator(artifactDaysToKeepStr: '', artifactNumToKeepStr: '5', daysToKeepStr: '', numToKeepStr: '5')
    disableConcurrentBuilds()
  }
  stages {
    stage('Hello'){
      steps{
        echo "Hello"
      }
    }
    stage('cat README'){
      when {
        branch "*123"
      }
      steps{
        sh '''
          cat README.md
        '''
      }
    }
  }
}
