pipeline {
    agent any

    stages {
        stage('scm') {
            steps {
        git branch: 'main', url: 'pipeline {
    agent any

    stages {
        stage('scm') {
            steps {
        git branch: 'main', url: 'https://github.com/nandhu6804/devops_main.git'
            }
        }
        stage('build') {
            steps {
               bat "mvn clean"
               bat "mvn install"
}
}
stage('build to images') {
            steps {
               script{
                  bat 'docker build -t nandhita22cse126/myapp .'
               }
    }
}
stage('push to hub') {
            steps {
               script{
                 withDockerRegistry(credentialsId: 'Docker_cred', url: 'https://index.docker.io/v1/') {
                  bat 'docker push nandhita22cse126/myapp'
               }
            }
            }
}
}
}'
            }
        }
        stage('build') {
            steps {
               bat "mvn clean"
               bat "mvn install"
}
}
stage('build to images') {
            steps {
               script{
                  bat 'docker build -t demohub/simplewebapp .'
               }
    }
}
stage('push to hub') {
            steps {
               script{
                 withDockerRegistry(credentialsId: 'Docker_cred', url: 'https://index.docker.io/v1/') {
                  bat 'docker push demohub/simplewebapp'
               }
            }
            }
}
}
}
