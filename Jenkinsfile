node {
    stage('git clone') {
    git credentialsId: 'tomcat_deployer', url: 'https://github.com/19Pushpa/ks.git'
    }
    stage('MAVEN Clean') {
    sh 'mvn clean'
 }
    stage('MAVEN Validate') {
    sh 'mvn validate'
 }
    stage('MAVEN Test') {
    sh 'mvn test'
 }
    stage('MAVEN Package') {
    sh 'mvn package'
 }
    stage('MAVEN Deploy') {
    sh 'mvn deploy'
  }
}