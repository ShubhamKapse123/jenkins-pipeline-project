pipeline{
  agent any
  // we can also define the other tools like docker, awd, others.
  tools{
    maven "maven"
  }
  environment{
    VERSION_APP="1.0"
  }
// we can define numbers of stages inside the stages
  stages{
    // we define the steps under the stage
    stage("compile"){
      when{
        expression{

        }
      }
      // define the steps
      steps{
        bat 'javac Test.java'
        bat 'echo ${VERSION_APP} '
      }
    }

    stage("run"){
      steps{
        bat "java Test"
      }
    }
  }
//this for post operation perform 
  post{

    always{
      bat 'echo "always" '
    }
    success{
      bat 'echo "success" '
    }
  }
}