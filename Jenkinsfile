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
      emailext body: 'test', subject: 'hi', to: 'sriban1805@gmail.com'
   }
}
