pipeline {
  agent any

  // Install the Jenkins tools you need for your project / environment
  tools {
    snyk 'Snyk' // Refers to a global tool configuration for Snyk called 'Snyk'
  }

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
