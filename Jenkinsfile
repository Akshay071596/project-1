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
					      sh" sudo yum install httpd -y"
						  sh"sudo service httpd start"
					 }
				
				
				}
                             stage("install-git"){
					steps{
					sh"sudo yum install git -y"

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
