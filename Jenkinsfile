node {
    stage('SCM Checkout') {
        git branch: 'main',
            url: 'https://github.com/kalpesheic/app.git'
    }

    stage('Compile-Package') {
        sh 'mvn package'
    }
}
    
