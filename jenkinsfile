pipeline {
    agent any
    stages {
        stage ('Fetch code') {
            steps {
                git branch: 'main', url: 'https://github.com/krsharathrao/jenkins-repo.git'
            }
        }
        stage ('Install apache') {
            steps {
                sh 'sudo apt install -y apache2'
            }
        }
        stage ('Deploy code') {
            steps {
                sh 'sudo cp -R * /var/www/html/'
            }
        }
    }
}
