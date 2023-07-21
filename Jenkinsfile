pipeline{
         agent{
		       label{ 
		           label"slave-1"
			   customWorkspace "/mnt/assignment-2"
			  }
	 }
		 stages{
		         stage("git-install"){
                             steps{
				     sh"sudo yum install git -y"

			     }
			 }
				stage("httpd-install-start"){
				     steps{
					      sh" sudo yum install httpd -y"
						  sh"sudo service httpd start"
					 }
				
				
				}
		        
				stage("deploy-index"){
				     steps{
					       sh"sudo chmod -R 777 /var/www/html"
						   sh"sudo cp index.html /var/www/html"
					 
					 }
				
				}
		 }
		 
}
