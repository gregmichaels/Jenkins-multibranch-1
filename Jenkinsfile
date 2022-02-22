pipeline {
  
    agent any
  
  stages {
    
    stage("build" {
      
      steps {
          echo 'building the application...'
      }
    }
          
     stage("test" {
      
      steps {
          echo 'testing the application...'
      }
    }
           
      stage("Run Snyk Scan") {
        steps {
           snykSecurity monitorProjectOnBuild: true, snykInstallation: 'snyk', snykTokenId: 'Snyk-Jenkins'
        }
     }
           
    stage("deploy" {
      
      steps {
          echo 'building the application...'
      }
    }
  }
}
