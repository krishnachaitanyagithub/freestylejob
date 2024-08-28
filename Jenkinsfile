node {
    
    // Checkout the code from version control
    stage('Checkout') {
          steps {
         git branch: 'main', url: 'https://github.com/krishnachaitanyagithub/freestylejob.git'
              checkout scm
    }
}

    // Build the project
    stage('Build') {
steps {
       sh 'javac Hello.java'
    }
}


    // Run tests
    stage('Test') {
steps {
        sh 'java Hello'
    }
}
       }
