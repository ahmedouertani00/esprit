pipeline {
    agent any

    stages {
        stage('Pull') {
            steps {
                echo 'Pulling..'
                script{
                	chekout([$class: 'GitSCM', branches: [[name: '*/master']],
              		userRemoteConfigs: [[
                    		 credentialsId: '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',
                    		 url: 'https://github.com/ahmedouertani00/esprit.git' ]]])
                }
            }
        }

    }
}
