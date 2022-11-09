node{
   stage('SCM Checkout'){
     git 'https://github.com/sriban18/myrepo.git'
   }
   stage('Compile-Package'){
      // Get maven home path
      def mvnHome =  tool name: 'maven-3', type: 'maven'   
      sh "${mvnHome}/bin/mvn package"
   }
   stage('Email Notification'){
      emailext attachLog: true, body: 'this is my test', compressLog: true, recipientProviders: [buildUser()], subject: 'hi test', to: 'sriban1805@gmail.com'
   }
}
