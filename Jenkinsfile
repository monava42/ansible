pipeline {
    agent {
        node { label 'agent1'}
    }
    stages {
    	stage('Launch ansible playbook'){
            steps {
                sh '''ansible-playbook -i ./inventory/hosts playbook.yml
		    '''
            }
        }
        stage('Integration test'){
	    steps {
	    	sh '''curl -I 172.17.0.9:80
		    '''
            }
	}
    }
}
