pipeline {
    agent any
    stages {
        stage('Test'){
            steps {
                git url: 'https://github.com/pandamys/example-playbook.git', branch: 'master'
                sh 'ansible-galaxy install -r requirements.yml'
                sh 'ansible-playbook site.yml -i inventory/prod.yml'
            }
        }
    }
}
