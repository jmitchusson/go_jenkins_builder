#!/usr/bin/env groovy

pipeline{
    agent{
        label "node"
    }
    stages{
        stage("A"){
            steps{
                checkout([$class: 'GitSCM', 
                branches: [[name: '*/master']], 
                doGenerateSubmoduleConfigurations: false, 
                extensions: [], 
                submoduleCfg: [], 
                userRemoteConfigs: [[credentialsId: 'justin_github', url: 'https://github.com/jmitchusson/go_jenkins_builder']]])
            }
        }
    }
}