node('docker-j') {
  stage('docker push') {
    sh 'docker version'
    git(url: 'https://github.com/pocteo/boilerplate-node-api.git', branch: '12_test_pr')
    sh 'docker login -u pocteo -p @hi_pocteo'
    sh 'docker build -t pocteo/boilerplate-node-api + ":$GITHUB_PR_NUMBER" .'
    sh 'docker push pocteo/boilerplate-node-api + ":$GITHUB_PR_NUMBER" '
  }
}
