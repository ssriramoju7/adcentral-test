node {
	
	stage('SCM Checkout'){

		git 'https://github.com/ssriramoju7/adcentral-test.git'

	}

	stage('Mvn Package'){
	   
	   sh 'mvn package -Denv=qa'
   }
}
