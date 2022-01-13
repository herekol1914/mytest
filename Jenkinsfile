node{
  stage('SCM Checkout'){
  git 'https://github.com/herekol1914/mytest/'
  }
  stage('Compile-Package'){
    //get maven homepath
    def mvnHome = tool name: 'maven-3', type: 'maven'
    sh "${mvnHome}/bin/mvn package"
  }
  stage('Email Notification'){
    mail bcc: '', body: '''Hi welcome to jenkins email alerts
    Thanks 
    herekol''', cc: '', from: '', replyTo: '', subject: 'Jenkins Job', to: 'daniel.casalis35@gmail.com'
  }
}
