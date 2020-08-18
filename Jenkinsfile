pipeline{
    agent any
    stages{
        stage('Build'){
            steps {
                echo "Build"
                powershell label: '', script: 'mvn clean package -f spring-boot-samples\\spring-boot-sample-atmosphere\\pom.xml'
            }
        }
        stage('Archive'){
            steps {
                echo "Archive"
                archiveArtifacts artifacts: 'spring-boot-samples/spring-boot-sample-atmosphere/target/*.jar', followSymlinks: false
            }
        }
        stage('Publish JUnit'){
            steps {
                echo "Publish JUnit"
            }
        }
        stage('Publish HTML'){
            steps {
                echo "Publishh HTML"
            }
        }
    }
}
