pipeline{
	agent any
	tools{
		maven 'maven'
		}
	stages{
		stage('checkout'){
		steps{
		git branch:'master',url='https://github.com/DivyanshuChauhan03/Ansible'
		}
		}
		stage('build'){
		steps{
		sh 'mvn clean install'
		}
		}
		stage('deploy'){
		steps{
		sh 'mvn clean package'
		sh 'ansible-playbook ansible/playbook.yml -i ansible/hosts.ini'
		}
		}
		}
		}
