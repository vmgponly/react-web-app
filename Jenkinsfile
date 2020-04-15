pipeline 
{
  agent any
  tools 
  {
    nodejs 'node'
  }
  
  stages
  {
    stage('Build')
    {
      steps
      {
        script 
        {
          checkout changelog: false, poll: false, scm: [$class: 'GitSCM', branches: [[name: '${RepoBranch}']], doGenerateSubmoduleConfigurations: false, extensions: [], submoduleCfg: [], userRemoteConfigs: [[credentialsId: 'git_cred', url: 'https://github.com/aniruddha-sinha/react-web-app.git']]]
        }
      }
    }
  }
}
