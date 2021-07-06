pipeline {
    agent any

    stages {
        stage('Quick Build') {
            steps {
                echo 'Building'
            }
            stage('OS') {
              steps {
                echo 'Build OS'
              }
            }
        }
        stage('Deploy to Dev') {
            // when {
            //     branch 'develop'
            // }
            stages {
                stage('Building Distributable Package') {
                    steps {
                        echo 'Building'
                    }
                }
                stage('Archiving Package') {
                    steps {
                        echo 'Archiving Aritfacts'
                    }
                }
                stage('Deploying Dev') {
                    steps {
                        echo 'Deploying'
                        timeout(time:3, unit:'DAYS') {
                            input message: "Approve build?"
                        }
                    }
                }
            }

        }
        stage('Deploy to Test') {
            when {
                branch 'develop'
            }
            steps {
                echo 'deploying..'
                timeout(time:3, unit:'DAYS') {
                    input message: "Approve build?"
                }
            }
        }
        stage('Deploy to Prod') {
            when {
                branch 'release'
            }
            steps {
                timeout(time:3, unit:'DAYS') {
                    input message: "Deploy to Prod?"
                }
                echo 'Deploying....'
            }
        }
    }
}
