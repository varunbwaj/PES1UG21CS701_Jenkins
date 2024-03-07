pipeline{
  agent any
  stages{
    stage("Build"){
      steps{
        build 'PES1UG21CS701-1'
        sh 'g++ hello.cpp -o working'
      }
    }
    stage("Test"){
      steps{
        sh './hello'
      }
    }
    stage("Deploy"){
      steps{
        echo 'Deploy'
      }
    }
  }
  post{
    failure{
      error 'Pipeline failed'
    }
  }
}
