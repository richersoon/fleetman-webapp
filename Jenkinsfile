node {
   stage('Preparation') { 
      git 'https://github.com/richersoon/fleetman-webapp.git'
   }
   stage('Build') {
      sh "mvn clean package"
   }
   stage('Results') {
      junit '**/target/surefire-reports/TEST-*.xml'
      archive 'target/*.jar'
   }
}
