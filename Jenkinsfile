node {
  stage('Checkout code') {
    git 'https://github.com/js73349/simple-java-maven-app'
  }
  stage('Compile code') {
    def mvnHome = tool name: 'maven-3.6.3', type: 'maven'
    sh "${mvnHome}/bin/mvn package"
    //sh 'mvn clean install'
  }
}
