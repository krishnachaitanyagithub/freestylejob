node {
    // Define workspace and ensure it's clean
    stage('Prepare') {
        deleteDir()  // Clean the workspace
        checkout scm  // Checkout source code from SCM
    }

    // Build stage
    stage('Build') {
        try {
            // Example of running a shell command
            sh 'echo Building...'
            sh 'make'  // Replace with your build command
        } catch (Exception e) {
            currentBuild.result = 'FAILURE'
            throw e  // Propagate the exception to fail the build
        }
    }

    // Test stage
    stage('Test') {
        try {
            // Example of running tests
            sh 'echo Running tests...'
            sh 'make test'  // Replace with your test command
        } catch (Exception e) {
            currentBuild.result = 'UNSTABLE'
            // Log the error and continue
            echo "Tests failed, but build is marked as UNSTABLE"
        }
    }

    // Deploy stage
    stage('Deploy') {
        // Example deployment command
        sh 'echo Deploying...'
        // Add your deployment steps here
    }
}
