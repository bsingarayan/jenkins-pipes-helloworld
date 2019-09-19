node {
  try {
    stage('checkout') {
      checkout scm
    }
    stage('prepare') {
      sh "git clean -fdx"
    }
    stage('compile') {
      echo "nothing to compile for hello.sh..."
    }
    stage('test') {
      sh "./test_hello.sh"
    }
    stage('package') {
      sh "tar -cvzf hello.tar.gz hello.sh"
    }
    stage('publish') {
      echo "uploading package..."
    }
    stage('Add some information') {
      sh "pwd"
      sh "ls -l ~/"
      sh "groovy -version"
      sh "uname -ai"
    }
  } finally {
    stage('cleanup') {
      echo "doing some cleanup..."
    }
  }
}
