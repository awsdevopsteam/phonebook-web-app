pipeline {
    agent any

    stages {
        stage('Checkout Code') {
            steps {
                script {
                    checkout scmGit(
                        branches: [[name: '*/master']],
                        extensions: [cloneOption(depth: 1, noTags: false, reference: '', shallow: true, timeout: 120)],
                        userRemoteConfigs: [[
                            url: 'https://github.com/awsdevopsteam/phonebook-web-app.git'
                        ]]
                    )
                }
            }
        }

        stage('Build') {
            steps {
                echo 'Building the application...'
                // Buraya ihtiyaç halinde derleme komutları eklenebilir, örneğin:
                // sh 'mvn clean package' (Java projeleri için)
                // sh 'npm install' (Node.js projeleri için)
            }
        }

        stage('Test') {
            steps {
                echo 'Running tests...'
                // Buraya test komutları eklenebilir, örneğin:
                // sh 'mvn test' (Java testleri için)
                // sh 'npm test' (Node.js testleri için)
            }
        }

        stage('Deploy') {
            steps {
                echo 'Deploying application...'
                // Buraya
