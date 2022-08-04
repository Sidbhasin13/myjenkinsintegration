pipeline {
  agent any
  environment {
    APPSYSID = '88466fae1b0111106deaff37dc4bcbea'
    BRANCH = "${BRANCH_NAME}"
    CREDENTIALS = 'Servicenow'
    DEVENV = 'https://dev92774.service-now.com/'
  }
  }
  stages {
    stage('Build') {
      when {
        not {
          branch 'master'
        }
      }
      def api = sh(script: """
          curl -k -u "${CREDENTIALS}"-X POST -H 'Content-Type: application/json' ${DEVENV}/api/now/table/incident --header -d '{"payload": {"short_description": "Sidharth test","urgency": "2","impact": "2"}}'
        """ 
      )
    }
  )
}
