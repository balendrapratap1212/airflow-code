pipeline {
  agent any
  environment{
    STORAGE_ACCOUNT_CREDENTIALS_DEV=credentials("storage_Account_credentials-dev")
    STORAGE_ACCOUNT_CREDENTIALS_QA=credentials("storage_Account_credentials-qa")
  }
  stages {
    stage('Deploy into Dev') {
      steps {
            
                echo "Balendra"
                sh 'az storage file upload-batch --destination airflow-dags --source dags --account-name $STORAGE_ACCOUNT_CREDENTIALS_DEV_USR --account-key $STORAGE_ACCOUNT_CREDENTIALS_DEV_PSW'
        }
    }
    stage('Deploy into QA'){
      steps{
        echo "Balendra"
                sh 'az storage file upload-batch --destination airflow-dags --source dags --account-name $STORAGE_ACCOUNT_CREDENTIALS_QA_USR --account-key $SSTORAGE_ACCOUNT_CREDENTIALS_QA_PSW'
      }
    }
    }
  }
