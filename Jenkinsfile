pipeline {
    agent any
    stages {
        stage ("SCM checkout") {
            steps {
                git "https://github.com/gopal1409/ansible-tomcat-jenkins-script.git"
                
            }
        }
        stage(" execute Ansible") {
           steps {
               sshagent(['ssh-pass-ansible']) {
                 ansiblePlaybook inventory:  'dev.inv', playbook: 'tomcat.yml'
              }
                
            }    
        }    
    }
}

