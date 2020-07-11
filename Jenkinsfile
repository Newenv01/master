node{
  stage('SCM Checkout'){
     sh "rm -f /var/lib/jenkins/workspace/NewPip/*.*"
     git "https://github.com/Newenv01/master.git"
     echo "Testing"
  }
  stage('Compile-Package'){
     echo "testdir"
     //sh "/usr/bin/bash /var/lib/jenkins/test.sh"
     //./test.sh
     sh "cd /var/lib/jenkins/workspace/NewPip"
     // sh "gzip *"
     }
   stage('Build'){
     echo "About to set variable"
     def mvnHome = tool name: 'maven-1', type: 'maven'
     sh "${mvnHome}/bin/mvn package"
     }

  stage('Sonar Analysis'){
     echo "Sonarqube Analysis"
     withSonarQubeEvn('SonarServer'){
     sh "${mvnHome}/bin/mvn sonar:sonar"
     }
  }
}
