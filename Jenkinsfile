pipeline {
 agent any
     stages {
            stage("Build") {
                steps {
                    sh 'php --version'
                    sh 'composer install'
                    sh 'composer --version'
                    sh 'cp .env.example .env'
                    sh 'php artisan key:generate'
                }
            }
            stage("Unit test") {
                 try {

                 }catch(ex){
                    echo 'something failed'
                     throw
                 }
                steps {
                    sh 'php artisan test'
                }

            }
     }
}

