pipeline {

    agent any


    stages {

        stage('Start Docker Container') {

            steps {

                sshagent(['ubuntu_docker']) {   #change_key_name

                    sh '''

                    ssh -o StrictHostKeyChecking=no ubuntu@54.82.85.32 "   #Change_public_ip

                    docker start fruitkha-website || true

                    "

                    '''

                }

            }

        }


        stage('Verify Running Container') {

            steps {

                sshagent(['ubuntu_docker']) {

                    sh '''

                    ssh -o StrictHostKeyChecking=no ubuntu@54.82.85.32 "   #Change_public_ip

                    docker ps

                    "

                    '''

                }

            }

        }

    }

}
