pipeline {
    agent any

    stages {
        stage('Hello') {
            steps {
                echo 'Hello World'
            }
        }

        stage('Parallel_stage') {
            parallel {
                stage(parallel_1) {
                    steps {
                        sh 'echo "Hello World"'
                    }
                }
                stage(parallel_2) {
                    steps {
                        sh '''
                        echo "Hello World"
                        touch new.txt
                        pwd
                        ls
                        '''
                    }
                }
            }
        }

        stage('Hello_Again_test') {
            steps {
                echo 'Hello World'
            }
        }
    }
}
