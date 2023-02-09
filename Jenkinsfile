pipeline {
  agent any
  environment{
    STORAGE_ACCOUNT_CREDENTIALS=credentials("storage_Account_credentials-dev")
  }
  stages {
    stage('Deploy into Dev') {
      steps {
            
                echo "Balendra"
                sh '''az storage file upload-batch --destination airflow-dags --source dags --account-name $STORAGE_ACCOUNT_CREDENTIALS_USR --account-key $STORAGE_ACCOUNT_CREDENTIALS_PSW'''
        }
    }
  }
  }