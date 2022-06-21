node {
  stage('SCM') {
    sh 'cd /var/jenkins/workspace'
    sh 'pwd'
    sh 'sudo rm -rf mysonarqube'
    sh 'git clone https://github.com/SivaKumar2606/MSBuild_sonarqubeproj1.git mysonarqube/'
  }
  stage('SonarQube Analysis') {
    def scannerHome = tool 'mysonarqube';
    withSonarQubeEnv() {
      sh "${scannerHome}/bin/sonar-scanner"
    }
  }
}
