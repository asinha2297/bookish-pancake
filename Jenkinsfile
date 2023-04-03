node {    
      def app     
      stage('Clone repository') {               
             
            checkout scm    
      }
	stage('Initialize'){
        def dockerHome = tool 'myDocker'
        env.PATH = "${dockerHome}/bin:${env.PATH}"
    	}     
      stage('Build image') {         
       
            app = docker.build("asinha2297/project1")    
       }     
      
       stage('Push image') {
       	docker.withRegistry('https://hub.docker.com/repositories/annusinha') { 
	    app.push("${env.BUILD_NUMBER}")
	   	}
       }
}
