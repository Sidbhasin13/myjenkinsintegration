pipeline {
  agent any
  environment {
    APPSYSID = '88466fae1b0111106deaff37dc4bcbea'
    BRANCH = "${BRANCH_NAME}"
    USERNAME = 'admin'
    PASSWORD = '*F08Glrf/jAQ'
    DEVENV = 'https://dev92774.service-now.com/'
  }
  stages {
    stage('Build') {
      when {
          branch 'master'
      }
      steps{
          basic(script: """ 
              HttpBasicAuth(str:${USERNAME}, str:${PASSWORD})
          """
          )
          sh(script: """
              curl -k -u "${basic}"-X POST -H 'Content-Type: application/json' ${DEVENV}/api/now/table/incident --header -d '{"payload": "short_description": "Sidharth test","urgency": "2","impact": "2"}'
            """ 
        )
      }
    }
  }
}
