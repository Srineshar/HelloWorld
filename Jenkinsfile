pipeline{
  agent any
   stages{
    stage('Checkout')
    {
      steps{
        checkout([$class: 'GitSCM', branches: [[name: '*/master']], doGenerateSubmoduleConfigurations: false, extensions: [], submoduleCfg: [], userRemoteConfigs: [[url: 'https://github.com/Srineshar/HelloWorld.git']]])
           }
      steps{
        workspace=pwd()
        }
    }
    stage("Checkpoint") {
      
      steps{
      checkpoint 'Completed Build'
      }
    }
    stage('Static Code Analysis')
    {
      steps{
        echo "Static Code Analysis"
      }
    }
    stage('Build')
    {
      steps{
        echo "Build the Code"
          }
    }
    stage('Unit Testing')
    {
      steps{
        echo "Unit testing"
        }
   }
    stage('Delivery')
    {
      steps{
        echo "Deliver the Code"
      }
    }
   }
}
