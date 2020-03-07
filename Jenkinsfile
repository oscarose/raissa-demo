pipeline {
    agent {
        label'master'
    }
    stages {
         stage('clone down scm') {
             steps {
                 git branch: 'master',
                 credentialsId: 'Github_ID',
                 url: 'https://github.com/oscarose/raissa-demo.git'
             }
         }
         stage('get install tools version') {
             steps {
                 sh """
                 which ansible
                 which docker
                 docker --version
                 ansible --version
                 git --version
                 """
             }
         }
    }
}
