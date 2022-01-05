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
   stage('SonarQube') {
        sh 'mvn sonar:sonar  -Dsonar.host.url=http://34.125.186.195:9000 -Dsonar.login=1cd1a086ad45914aac5f7a2103d43f932ae0f5d8'
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
