node ('NuevoNodo') {
    stage('Clonacion Repositorio') {
        git branch: 'master',
            credentialsId: 'githubssh',
            url: 'git@github.com:CamilaEscuderoC/DVWA.git'

        sh "ls -lat"
        
    }
    stage('Test Unitarios') {
        sh 'echo "Tests passed Hola mundo"'
    }
    stage('Analisis de Codigo con Sonar') {
//        sh '$sonar_slave/sonar-scanner -Dsonar.projectKey=CAMILA -Dsonar.source=. -D sonar.login=ccfc56a1958421dcd3580fd1733942d1b66546c4 -Dproject.settings=./sonar-project.properties'
    }
    stage('Deploy sobre EC2') {
        sh 'docker ps'
    }
    stage('Send slack notification') {
         slackSend color: 'good', message: 'Message from Jenkins Pipeline'
    }
}
