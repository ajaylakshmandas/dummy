pipeline {
    agent any

    stages {
        stage('build') {
            steps {
                echo 'b World'
            }
        }
        stage('test') {
            steps {
                echo 't World'
            }
        }
        stage('deploy') {
            steps {
                echo 'd World'
            }
        }
    }
    post{
    always{
        emailext body: 'notify', subject: 'smart', to: 'ajaydevops26@gmail.com'
    }
 } 
     post{
    success{
       build quietPeriod: 1, job: 'car'
    }
 } 
}
