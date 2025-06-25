pipeline{
    tools{
        jdk 'java'
        maven 'maven'
    }
	agent any
      stages{
           stage('Checkout'){
              steps{
		 echo 'cloning..'
                 git 'https://github.com/magmomo2025/Myfirstrepo.git'
              }
          }
          stage('Compile with maven'){
              steps{
                  echo 'compiling..'
                  sh 'mvn compile'
	      }
          }
          stage('CodeReview with maven'){
              steps{
		    
		  echo 'codeReview'
                  sh 'mvn pmd:pmd'
              }
          }
          
          stage('Package with maven'){
              steps{
                  sh 'mvn package'
              }
          }
      }
}
