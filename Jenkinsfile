pipeline {
  agent {
    kubernetes {
      //cloud 'kubernetes'
      label 'mypod'
      containerTemplate {
        name 'maven'
        image 'maven:3.3.9-jdk-8-alpine'
        ttyEnabled true
        command 'cat'
      }
    }
  }
  stages {
  steps('CheckOut'){
            container('jnlp'){
                 git([url: 'https://github.com/pmajum/jenkins-build.git', branch: 'master'])
            }
           
           
        }
       
        steps ('Build') {
            container('maven') {
            
            sh 'ls -lat'
          }
        }
  
  }
}
