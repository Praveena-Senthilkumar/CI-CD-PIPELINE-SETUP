pipeline {
    agent any

    stages {
        stage('Checkout') {
            steps {
                git 'https://github.com/your-repo.git'
            }
        }

        stage('Build') {
            steps {
                sh 'npm install'  // Adjust based on your tech stack
            }
        }

        stage('Test') {
            steps {
                sh 'npm test'  // Run tests (modify as needed)
            }
        }

        stage('Deploy') {
            steps {
                sshagent(['your-ssh-credential-id']) {
                    sh 'scp -r * user@server:/var/www/app'
                }
            }
        }
    }
}
