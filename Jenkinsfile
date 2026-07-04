node {
    stage('SCM Checkout') {
        git branch: 'main',
            url: 'https://github.com/kalpesheic/app.git'
    }

    stage('Compile-Package') {
        def mvnHome = tool name: 'maven-3', type: 'maven'
        sh "${mvnHome}/bin/mvn clean package"
    }
}

   stage('Slack notification') {
       slackSend baseUrl: 'https://hooks.slack.com/services/', 
           botUser: true, channel: '#devops',
           color: 'good', 
           message: 'welcome to slack', 
           tokenCredentialId: 'slack-demo'
   }
       
    
