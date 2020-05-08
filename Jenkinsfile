pipeline {
      agent any
      stages {
            stage('Uploade to AWS'){
                  steps {
                        withAWS(region:'us-west-1',credentials:'aws-static') {
                            sh 'echo "Uploading content with AWS creds"'
                                s3Upload(pathStyleAccessEnabled: true, payloadSigningEnabled: true, file:'index.html', bucket:'jenkinsproject0508')
                        }
                  }
            }
      }
}
