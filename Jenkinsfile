pipeline {
  
  agent any
  
  parameters {
    string( name: 'semver', defaultValue: '1.0.0', description: 'the resulting semver version number after running gitversion on the source at GitHub')
    string( name: 'branchname', defaultValue: 'master', description: 'the actual branch name that triggered the build as precurred from gitVersion')
  }
  
  stages {
    stage('Initialization') {
      steps {
        buildName "${params.semver}"
        buildDescription "${params.branchname}"
      }
    }
  }
}
