pipeline {
    agent any
    
    stages {
        stage('checkout_source') {
            steps {
                checkout([$class: 'GitSCM',
                    branches: [[name: '*/feature/Jenkinsfile']],
                    doGenerateSubmoduleConfigurations: false,
                    extensions: [],
                    submoduleCfg: [],
                    userRemoteConfigs: [[
                        credentialsId: '8c8e4bd9-e12e-413c-95af-ede6b7e7c267',
                        url: 'https://github.com/jmitchusson/go_jenkins_builder'
                        ]]])
            }uil
        }
        stage('build') {
            steps {
                go build
                ./go_jenkins_builder
            }
        }
    }
}