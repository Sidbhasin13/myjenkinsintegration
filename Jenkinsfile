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
          sh(script: """
              curl -X POST https://${USERNAME}:${PASSWORD}@${DEVENV}/api/now/table/incident --data-raw json='{"parameter": [{"short_description": "Sidharth test2","urgency": "2","impact": "2"}]}'
            """ 
        )
      }
    }
  }
}
