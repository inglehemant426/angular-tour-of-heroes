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
        
        
    }
}
