node('master') {

   stage 'Git Checkout'
	 git 'https://github.com/mrdevtechnology/dryRun.git'
         echo 'checkout done'
   
   stage 'Ansible Playbook'
         ansiblePlaybook colorized: true, inventory: '~/${env.JOB_NAME}/inventory/dev', playbook: '~/${env.JOB_NAME}/site.yml', sudo: true, sudoUser: null
         echo 'maven validate'
   
   stage 'Job Status Status'
    	echo 'Done'            
}
