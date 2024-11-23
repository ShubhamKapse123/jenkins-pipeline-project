pipeline{
  agent any
  environment{
    VERSION_APP="1.0"
  }

  stages{
    stage("compile"){
      steps{
        bat 'javac Test.java'
        bat 'echo "${VERSION_APP}"'
      }
    }

    stage("run"){
      steps{
        bat "java Test"
      }
    }
  }

  post{

    always{
      bat 'echo "always" '
    }
    success{
      bat 'echo "success" '
    }
  }
}