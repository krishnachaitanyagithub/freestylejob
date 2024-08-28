node {
// Define the workspace directory
def workspace = pwd()

try {
// Stage to checkout the code from GitHub
stage('checkout') {
    checkout scm
}

// Stage to compile the Java code
stage('Build') {
    sh 'javac Hello.java'
}

// Stage to run the java application
stage('Run') {
    sh 'java Hello'
}
}
}
