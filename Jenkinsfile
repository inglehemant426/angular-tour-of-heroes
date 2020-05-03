pipeline {
    agent any
    stages {
        
        stage ('scm checkout') {
            steps {
                git branch: 'master', url: 'https://github.com/inglehemant426/angular-tour-of-heroes/'
            }
        }
        
        stage ('build') {
            steps {
                nodejs('npm') {
                    sh 'npm run build'
                }
            }
        }
        
        /*stage ('test') {
            steps {
                withMaven(jdk: 'localJDK', maven: 'localmaven') {
                    sh 'npm run test'
                }
            }
        }
         
        stage ('deploy to tomcat server') {
            steps {
               sshagent(['deploytomcat']) {
                    sh 'scp -o StrictHostKeyChecking=no */target/*.war ec2-user@172.31.86.233:/var/lib/tomcat/webapps'
                }
            }
        }*/
    }
}
