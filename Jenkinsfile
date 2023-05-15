node {    
      def app     
      stage('Clone repository') {               
             
            checkout scm    
      }
	//stage('Initialize'){
        //def dockerHome = tool 'myDocker'
        //env.PATH = "${dockerHome}/bin:${env.PATH}"
    	//}     
      stage('Build image') {         
       
            app = docker.build("annusinha/project1")    
       }     
      
//        stage('Push image') {
//        	withDockerRegistry([ credentialsId: "dockerhub", url: "" ]) {
//         app.push()
// 	   	}
//        }
}
