node {	
	stage('SCM Checkout'){
		git 'https://github.com/ssriramoju7/adcentral-test.git'
	}
	stage('Mvn Perform Munit Testing'){
	   def mvnHome= tool name: 'maven', type: 'maven'   
	   sh "${mvnHome}/bin/mvn test -Denv=qa"
  	}
	stage('Mvn Deploy'){
	   def mvnHome= tool name: 'maven', type: 'maven'   
	   sh "${mvnHome}/bin/mvn deploy -Denv=qa"
   	}
}
