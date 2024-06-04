pipeline{
  agent any

  stages{
    stage('Run test 1'){
      steps{
        sh """
          chmod u+x test1.sh
	  ./test1.sh
	   """
      }
    }
    stage('Run test 2'){
      steps{
        sh './test2.sh'
      }
    }
    stage('Run test 3'){
      steps{
        sh './test3.sh'
      }
    }
  }
}
