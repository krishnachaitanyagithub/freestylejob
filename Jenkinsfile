node {
    
    // Checkout the code from version control
    stage('Checkout') {
      checkout scm
    }

    // Build the project
    stage('Build') {
       sh 'javac Hello.java'
    }


    // Run tests
    stage('Test') {
        sh 'java Hello'
    }
       }
