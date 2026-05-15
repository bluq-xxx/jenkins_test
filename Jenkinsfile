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
            }
        }
    }
}
