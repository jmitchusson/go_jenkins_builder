#!/usr/bin/env groovy

pipeline{
    agent "any"

    stages {
        stage('Checkout: Code') {
            steps {
                sh " git clone 'https://github.com/jmitchusson/go_jenkins_builder.git'"
            }
        }
    }
}