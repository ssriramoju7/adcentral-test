node {	
	stage('SCM Checkout'){
		git 'https://github.com/ssriramoju7/adcentral-test.git'
	}
	stage('Mvn Perform Munit Testing'){
	   def mvnHome= tool name: 'maven', type: 'maven'   
	   sh "${mvnHome}/bin/mvn test -Denv=qa"
  	}
	
	stage('Anypoint CLI Login'){  
	   sh "which anypoint-cli"
	   sh "anypoint-cli --username=srikanth-mulesoft --password=Rockstar7*"
	   echo "pwd"
	   sh "pwd"
	  echo " below is list of applications deployed"
	  sh "rm -rf commandResultFile"
	  def script = sh "anypoint-cli --username=srikanth-mulesoft --password=Rockstar7* --environment Sandbox runtime-mgr standalone-application list -o text -f Application > commandResultFile"
	  sh "anypoint-cli --username=srikanth-mulesoft --password=Rockstar7* --environment Sandbox runtime-mgr standalone-application list"
	  echo "$script"
	  def applicationsList = readFile('commandResultFile').trim()
	  echo "applicationsList is $applicationsList"

  	}
	
	//stage('Mvn Deploy'){
	  // def mvnHome= tool name: 'maven', type: 'maven'   
	   //sh "${mvnHome}/bin/mvn deploy -Denv=qa"
   	//}
}



