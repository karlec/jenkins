#!/usr/bin/env groovy
pipeline {
    agent any

    environment {
        TEST_PREFIX = "test-IMAGE"
        TEST_IMAGE = "${env.TEST_PREFIX}:${env.BUILD_NUMBER}"
        TEST_CONTAINER = "${env.TEST_PREFIX}-${env.BUILD_NUMBER}"
        REGISTRY_ADDRESS = "my.registry.address.com"

        SLACK_CHANNEL = "#deployment-notifications"
        SLACK_TEAM_DOMAIN = "MY-SLACK-TEAM"
        // SLACK_TOKEN = credentials("slack_token")
        DEPLOY_URL = "https://deployment.example.com/"

        COMPOSE_FILE = "docker-compose.yml"
        // REGISTRY_AUTH = credentials("docker-registry")
        STACK_PREFIX = "my-project-stack-name"
    }

    stages {
        stage("Prepare") {
            steps {
                echo "INPROGRESS"
                echo TEST_IMAGE
            }
        }

        stage("seguimos") {
            steps {
                echo "va todo bien"
            }
        }
    }

    post {
        always {
            echo 'empezamosss'
        }

        success {
            echo "SUCCESSFUL"
        }

        failure {
            echo "FAILED"
        }
    }
}