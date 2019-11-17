node {
    stage('vcs') {
      git 'https://github.com/Nara-Sagar7/Shopiazer-Project.git'
   }
   
    stage('Build') {
      sh'mvn package'
   }
   
    stage('QA Gate') {
      withSonarQubeEnv('sonar'){
          sh 'mvn org.sonarsource.scanner.maven:sonar-maven-plugin:3.2:sonar'
      }
   }
   
}
