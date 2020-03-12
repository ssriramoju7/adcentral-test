node {
	
	stage('SCM Checkout'){

		git 'https://github.com/ssriramoju7/adcentral-test.git'

	}

	stage('Mvn Package'){

	   def mvnHome= tool name: 'maven', type: 'maven'   
	   sh "${mvnHome}/bin/mvn package -Denv=qa"
   }
}
