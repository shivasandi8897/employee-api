pipeline {
  agent any
  
  stages {
  stage('Build') {
     steps {
       bat 'mvn -B -U -e -V clean -DskipTests package'
     }
  }
  stage('Test') {
      steps {
    echo "******* munit test cases execution ******"
    }
  }
 stage('Deployment') {
 
  steps {
  bat 'mvn -U -V -e -B -DskipTests deploy -Ptest -DmuleDeploy
  }
 }
 
  }
}