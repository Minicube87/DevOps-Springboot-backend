pipeline{

    agent any

    tools{
      maven 'Maven'
    }

    stages{

        // Ziehe Code aus Repo
        stage("Compile"){
          steps{
            sh "mvn compile"
          }
        }

        // Baue die Anwendung
        stage("Build"){
          steps{
            sh "mvn clean package"
          }
        }

        stage("Dependencies"){
          steps{
            sh "mvn test"
          }
        }
    }


    post{
        always{
            echo "================"
        }
        success{
            cleanWs()
        }
        failure{
            echo "========pipeline execution failed========"
        }
    }
}
