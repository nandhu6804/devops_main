pipeline {
    agent any

    stages {
        stage('scm') {
            steps {
        git branch: 'master', url: 'https://github.com/nandhu6804/devops_main.git'
            }
        }
        stage('build') {
            steps {
               sh "mvn clean"
               sh "mvn install"
}
}
stage('build to images') {
            steps {
               script{
                  sh 'docker build -t nandhita22cse126/mywebapp .'
               }
    }
}
stage('push to hub') {
            steps {
               script{
                 withDockerRegistry(credentialsId: 'Docker_cred', url: 'https://index.docker.io/v1/') {
                  sh 'docker push nandhita22cse126/mywebapp'
               }
            }
            }
}
}
}
