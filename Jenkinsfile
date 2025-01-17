pipeline {
    agent none
    stages {
        stage('Non-Parrallel Stage') {
            steps {
                echo "This agent will be executed first."
            }
        }
        stage('Run Tests') {
            parallel {
                stage('Test on Windows') {
                    agent {
                        label "Windows_Node1"
                    }
                    steps {
                        echo "Task1 on Agent"
                    }
                }
                stage('Test on Master') {
                    steps {
                        echo "Task1 on Master"
                    }
                }
            }
        }
    }
}
