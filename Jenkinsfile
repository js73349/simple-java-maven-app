node {
  stage('Checkout code') {
    git 'https://github.com/js73349/simple-java-maven-app'
  }
  stage('Compile code') {
    sh 'mvn clean install'
  }
}
