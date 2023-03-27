node {    
      def app     
      stage('Clone repository') {               
             
            checkout scm    
      }     
      stage('Build image') {         
       
            app = docker.build("annusinha/project1")    
       }     
      
       stage('Push image') {
       	docker.withRegistry('https://hub.docker.com/') { 
	    app.push("${env.BUILD_NUMBER}")
	   	}
       }
}
