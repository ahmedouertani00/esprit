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
			sh "ansible-playbook Ansible/roles/build.yml -i Ansible/inventory/host.yml"
		       }
		 }
	}

    }
}
