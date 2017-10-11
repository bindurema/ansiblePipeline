node('master') {

   stage 'Git Checkout'
	 git 'https://github.com/mrdevtechnology/dryRun.git'
         echo 'checkout done'
   
   stage 'Ansible Playbook'
         ansiblePlaybook colorized: true, inventory: '/var/lib/jenkins/workspace/${JOB_NAME}/inventories/dev', playbook: '/var/lib/jenkins/workspace/${JOB_NAME}/site.yaml', sudo: true, sudoUser: null
         echo 'maven validate'
   
   stage 'Job Status Status'
    	echo 'Done'            
}
