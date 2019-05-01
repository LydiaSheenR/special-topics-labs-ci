
node {
  stage('checkout sources') {
        git url: 'https://github.com/LydiaSheenR/special-topics-labs-ci'
  }

  stage('Build') {
    withMaven (maven: 'maven3') {
              sh "mvn package"
    }

  }

  {
              junit 'target/surefire-reports/*.xml'
          
  }
}
