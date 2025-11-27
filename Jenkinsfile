pipeline{

    agent any

    tools{
      maven 'Maven'
    }

    stages{

        // Ziehe Code aus Repo
        stage("Compile"){
          steps{
            dir('springboot-backend'){
                sh "mvn compile"
            }
          }
        }

        // Baue die Anwendung
        stage("Build"){
          steps{
            dir('springboot-backend'){
                sh "mvn clean package"
            }
          }
        }

        stage("Test"){
          steps{
            dir('springboot-backend'){
                sh "java -version"
                sh "mvn test"
            }
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
