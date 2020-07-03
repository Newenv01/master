node{
  stage('SCM Checkout'){
     git "https://github.com/Newenv01/master.git"
     echo "Testing"
  }
  stage('Compile-Package'){
     echo "testdir"
     sh "/usr/bin/bash /var/lib/jenkins/test.sh"
     //./test.sh
     }
}
