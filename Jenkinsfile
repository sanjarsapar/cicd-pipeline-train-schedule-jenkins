pipeline{
    agent any
    stages{
        stage("Build"){
            steps{
                echo "=== Executing Build ==="
                sh './gradlew build --no-daemon'
                archiveArtifacts artifacts: 'dist/trainSchedule.zip'
                sh 'ls -l'
                echo 'SUCCESSS!!!!!!!'
            }
            post{
                always{
                    echo "========Always========"
                }
                success{
                    echo "========Build executed successfully========"
                }
                failure{
                    echo "========Build execution failed========"
                }
            }
        }
    }
    post{
        always{
            echo "========Always========"
        }
        success{
            echo "========pipeline executed successfully ========"
        }
        failure{
            echo "========pipeline execution failed========"
        }
    }
}