
node {
  stage('checkout sources') {

        git url: 'https://github.com/jschmersal-cscc/special-topics-labs-quality'
  }

  stage('Build') {

    echo "hello"
    withMaven (maven: 'maven3') {
              sh "mvn package"
            }

  }
 
  post {
          always {
              junit '/home/lrhymond/IdeaProjects/special-topics-labs-ci/target/surefire-reports
'
          }
      }
}
