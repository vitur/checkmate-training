#!/usr/bin/env groovy

def options = '-Si'
def properties = "-PbuildId=${env.BUILD_TAG}"
def checkmate = "gradlew ${options} ${properties}"

pipeline {
    agent any

    stages {
        stage('Build') {
            steps {
                bat "${checkmate} metadataBuild"
            }
        }
    }
}