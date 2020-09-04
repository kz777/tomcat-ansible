pipeline {
    agent any

    stages {
        stage('SCM') {
            steps {
                git 'https://github.com/kz777/tomcat-ansible.git'
            }
        }
        stage('TOMCAT WITH ANSIBLE') {
            steps {
                ansiblePlaybook become: true, colorized: true, installation: 'ansible', inventory: 'hosts', playbook: 'tomcat-setup.yml'
            }
        }
    }
}
