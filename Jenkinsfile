node {
  state ('Checkout Code') {
    git 'https://github.com/jenkins-docs/simple-java-maven-app'
  }
  state ('Compile Code') {
    sh 'mvn clean install'
  }
}
