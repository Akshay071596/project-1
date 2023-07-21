pipeline{
         agent{
		       label {
			       label"built-in"
			   customWorkspace "/mnt/assignment-1"
			  }
	 }
		 
		 stages{
		 
				stage("build"){
				     steps{
					       sh"build"
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
