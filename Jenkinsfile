#!/usr/bin/env groovy

def path = "C:\git\checkmate-obi-training"
def options = '-Si'
def properties = "-PbuildId=${env.BUILD_TAG}"
def checkmate = "${path}\gradlew ${options} ${properties}"

pipeline {
    agent {
        label 'master'
    }

    stages {
        stage('Build') {
            steps {
                bat"${checkmate} metadataBuild"
            }
        }
        stage('Test') {
            steps {
                echo 'Testing..'
            }
        }
        stage('Publish') {
            steps {
                echo 'Building..'
            }
        }
        stage('Deploy') {
            when {
                branch 'master'
             }
            steps {
                echo 'Deploying..'
            }
        }
    }
}