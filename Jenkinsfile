pipeline{
         agent{
		       label{ 
		           label"slave-1"
			   customWorkspace "/mnt/assignment-2"
			  }
	 }
		 stages{
		         stage(git-install){
                             steps{
				     sh"sudo yum install git -y"

			     }
			 }
				stage("httpd-install-start"){
				     steps{
					      sh"yum install httpd -y"
						  sh"service httpd start"
					 }
				
				
				}
		        
				stage("deploy-index"){
				     steps{
					       sh"chmod -R 777 /var/www/html"
						   sh"cp index.html /var/www/html"
					 
					 }
				
				}
		 }
		 
}
