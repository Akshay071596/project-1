pipeline{
         agent{
		       label{ 
		           label"slave-2"
			   customWorkspace "/mnt/assignment-2"
			  }
	 }
		 stages{
		 
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
