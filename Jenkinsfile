pipeline{

    agent any

    stages{

        stage('Build Jar'){
            steps{
                sh "mvn clean package -DskipTests"
            }
        }

        stage('Build Image'){
            steps{
                sh "docker build -t=ufanarda/selenium"
            }
        }

        stage('Push Image'){
            steps{
                echo "docker push ufanarda/selenium ."
            }
        }

    }


}