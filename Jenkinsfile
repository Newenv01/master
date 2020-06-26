node{
  stage('SCM Checkout'){
     git 'https://github.com/Newenv01/master'
  }
  stage('Compile-Package'){
     sh 'nvn clean package'
  }
}
