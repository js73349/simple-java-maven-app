node {
  stage('Checkout code') {
    git 'https://github.com/js73349/simple-java-maven-app'
  }
  stage('Compile code') {
    def mvnHome = tool name: 'maven-3.6.3', type: 'maven'
    sh "${mvnHome}/bin/mvn clean install"
    //sh "${mvnHome}/bin/mvn package"
  }
  stage('Deploy') {
    sshagent(['tomcat-dit']) {
      sh 'scp -o StrictHostKeyChecking=no -l target/*.war jeffsmith@desktop-r08eqpu.usla.ibm.com:"/c/Program Files/Apache Software Foundation/Tomcat 7.0/webapps/"'
      //sh 'scp -o StrictHostKeyChecking=no -l target/*.war jeffsmith@9.70.98.139:"/c/Program Files/Apache Software Foundation/Tomcat 7.0/webapps/"'
    }
  }
}
