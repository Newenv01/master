node{
  stage('SCM Checkout'){
     sh "rm -f /var/lib/jenkins/workspace/NewPip/*.*"
     git "https://github.com/Newenv01/master.git"
     echo "Testing"
  }
  stage('Compile-Package'){
     echo "testdir"
     sh "/usr/bin/bash /var/lib/jenkins/test.sh"
     //./test.sh
     sh "cd /var/lib/jenkins/workspace/NewPip"
     sh "gzip *"
     }
}
