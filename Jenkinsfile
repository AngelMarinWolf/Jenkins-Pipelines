pipeline {
  agent none
  stages {
    stage('DevelopDeploy'){
      agent { node {label 'dev'} }
      when {
        branch 'dev'
      }
      steps{
        sh 'ls -lha'
        sh 'cp index.html /usr/share/nginx/html/pipeline/index.html'
      }
    }
    stage('TestDeploy'){
      agent { node {label 'test'} }
      when {
        branch 'master'
      }
      steps{
        sh 'ls -lha'
        sh 'cp index.html /usr/share/nginx/html/pipeline/index.html'
      }
    }
  }
}
