pipeline {
  agent any
  environment {
    APPSYSID = '88466fae1b0111106deaff37dc4bcbea'
    BRANCH = "${BRANCH_NAME}"
    CREDENTIALS = 'Servicenow'
  }
  }
  stages {
    stage('Build') {
      when {
        not {
          branch 'master'
        }
      }
      steps{
          curl --request POST 'https://dev92774.service-now.com/api/now/table/incident' --header 'Content-Type: application/json' --data-raw '{short_description": "Sidharth test","urgency": "2","impact": "2"}'
      }
    }
  )
}
