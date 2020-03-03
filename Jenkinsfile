def workspace;

node{
    
    stage('Checkout')
    {
        checkout([$class: 'GitSCM', branches: [[name: '*/master']], doGenerateSubmoduleConfigurations: false, extensions: [], submoduleCfg: [], userRemoteConfigs: [[url: 'https://github.com/Srineshar/HelloWorld.git']]])
        workspace=pwd()
        
    }
    stage("Checkpoint") {
      agent none //running outside of any node or workspace
      
      checkpoint 'Completed Build'
      
    }
    stage('Static Code Analysis')
    {
        echo "Static Code Analysis"
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
