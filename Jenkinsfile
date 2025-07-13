pipeline {
  agent any

  tools{
    maven 'Maven 3.9.6'
  }

  stages{
      stage("build"){
          steps{
              echo 'Compiling sysfoo app..'
              sh 'mvn compile'
          }
      }
      stage("test"){
          steps{
              echo 'Running unit tests...'
              sh 'mvn clean test'
          }
      }
      stage("package"){
          steps{
              echo 'Packaging sysfoo app'
              sh 'mvn package -DskipTests'
          }
      }
  }

  post{
    always{
        echo 'This pipeline is completed..'
    }
  }
}
