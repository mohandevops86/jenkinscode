pipeline {
  agent {
    node {
      label 'master'
    }
    
  }
  stages {
    stage('Build') {
      parallel {
        stage('Build') {
          agent {
            node {
              label 'MAVEN'
            }
            
          }
          steps {
            git(url: 'https://github.com/cit-latex/t1-student-maven-proj.git', branch: 'master')
            sh 'mvn compile package'
          }
        }
        stage('Test') {
          agent {
            node {
              label 'MAVEN'
            }
            
          }
          steps {
            sh 'ls'
          }
        }
      }
    }
  }
}