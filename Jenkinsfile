def workspace;

node{
    
    stage('Checkout')
    {
        checkout([$class: 'GitSCM', branches: [[name: '*/master']], doGenerateSubmoduleConfigurations: false, extensions: [], submoduleCfg: [], userRemoteConfigs: [[url: 'https://github.com/Srineshar/HelloWorld.git']]])
        workspace=pwd()
        
    }
   
    stage('Static Code Analysis')
    {
        echo "Static Code Analysis"
        steps {
        checkpoint 'Completed Build'
      }
    }
    stage('Build')
    {
        echo "Build the Code"
    }
    stage('Unit Testing')
    {
        echo "Unit testing"
    }
    stage('Delivery')
    {
        echo "Deliver the Code"
    }
}
