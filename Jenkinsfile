pipeline {
    agent any

    stages {
        stage('build') {
            steps {
                echo "Build sample-book-app.. "
            }
        }
        stage('deploy-dev') {
            steps {
                script{
                    deploy("DEV")
                }
            }
        }
        stage('api-test-dev') {
            steps {
                echo "API Tests triggered against DEV environemnt.. "
            }
        }
        stage('deploy-stg') {
            steps {
                script{
                    deploy("STG")
                }
            }
        }
        stage('api-test-stg') {
            steps {
                echo "API Tests triggered against STG environemnt.. "
            }
        }
        stage('deploy-prd') {
            steps {
                script{
                    deploy("PRD")
                }
            }
        }
        stage('api-test-prd') {
            steps {
                echo "API Tests triggered against PRD environemnt.. "
            }
        }
    }
}

def deploy(String enviroment){
    echo "Deployment triggered to ${enviroment} environemnt.. "
}

// Build of application;
//  deployment in “DEV” env;
// Test execution against DEV env;
//  deployment in “STG” env;
// Test execution against STG env;
//  deployment in “PRD” env;
// Test execution against PRD env.
