pipeline {
  agent any
  environment {
    APPSYSID = '88466fae1b0111106deaff37dc4bcbea'
    BRANCH = "${BRANCH_NAME}"
    USERNAME = 'admin'
    PASSWORD = 'Password'
    DEVENV = 'dev92774.service-now.com/'
  }
  stages {
    stage('Build') {
      when {
          branch 'master'
      }
      steps{
          sh(script: """
              curl -X POST https://${USERNAME}:${PASSWORD}@${DEVENV}/api/now/table/incident -H 'Content-Type: application/json' --data-raw '{"short_description": "POC Vulnerability Incident","urgency": "2","impact": "2"}}'
            """ 
        )
      }
    }
  }
}
