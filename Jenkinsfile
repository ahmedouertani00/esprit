pipeline {
    agent any

    stages {
        stage('Pull') {
            steps {
                echo 'Pulling..'
                script{
                	checkout([$class: 'GitSCM', branches: [[name: '*/master']],
              		userRemoteConfigs: [[
                    		 credentialsId: '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',
                    		 url: 'https://github.com/ahmedouertani00/esprit.git' ]]])
                }
            }
        }

    }
}
