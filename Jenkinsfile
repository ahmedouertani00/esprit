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
         
        stage('build') {
	    steps{
	    	echo 'Building..'
		script {
			sh "ansible-playbook Ansible/roles/build.yml -i Ansible/inventory/host.yml "

		       }
		 }
	}

    }
}
